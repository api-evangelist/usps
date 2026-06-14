# USPS GraphQL Schema

Conceptual GraphQL schema for the United States Postal Service (USPS) APIs. This schema models the capabilities exposed by the USPS REST API developer portal at [https://developer.usps.com/](https://developer.usps.com/), covering address validation, package tracking, label creation, domestic pricing, pickup scheduling, post office location, and service standards.

## Background

USPS offers a modern suite of RESTful APIs that replace the legacy Web Tools platform. Authentication is handled via OAuth 2.0 Client Credentials (the `Token` and `APIKey` types). The APIs cover:

- **Addresses** — validate and standardize US addresses to USPS specifications
- **Tracking** — retrieve tracking events and delivery status for USPS-shipped packages
- **Labels** — create and cancel domestic shipping labels with integrated pricing
- **Prices** — query current domestic pricing for any mail class and package type
- **Pickup** — check availability, schedule, update, and cancel carrier pickups
- **Post Offices** — locate nearby post offices with hours and services
- **Service Standards** — estimate delivery windows between origin and destination ZIP codes

## Schema Overview

### Authentication

| Type | Description |
|------|-------------|
| `APIKey` | Client credentials (ID + secret + scopes) used to request tokens |
| `Token` | OAuth 2.0 bearer token returned by the `/oauth2/v3/token` endpoint |

### Address Types

| Type | Description |
|------|-------------|
| `Address` | Full USPS-standardized address with DPV and carrier route fields |
| `AddressValidation` | Input/corrected address pair with additional validation metadata |
| `AddressAdditionalInfo` | DPV confirmation, LACS link, footnotes, and EWS indicator |
| `CityState` | City and state resolved from a ZIP code lookup |
| `ZipCode` | Basic ZIP code record with type and county |
| `ZipCodeDetails` | Full ZIP code details including all cities and counties served |
| `ZipCodeType` | Enum: UNIQUE, PO_BOX, MILITARY, STANDARD |

### Tracking Types

| Type | Description |
|------|-------------|
| `TrackingNumber` | Parsed tracking number with carrier and label class |
| `TrackingSummary` | Full tracking summary including expected delivery and events |
| `TrackingDetail` | Detailed tracking record with event history and alerts |
| `TrackingEvent` | Individual scan event with timestamp, location, and event code |
| `EventType` | Event code and human-readable description |
| `EventCity` | City name for a tracking event |
| `EventState` | State abbreviation and name for a tracking event |
| `EventZip` | ZIP code for a tracking event location |
| `EventCountry` | Country name and ISO alpha-2 code for international events |

### Package Types

| Type | Description |
|------|-------------|
| `Package` | Package description with mail class, type, weight, and dimensions |
| `PackageType` | Enum of USPS package types (flat rate, cubic, letter, parcel, etc.) |
| `FlatRate` | Flat rate container code, name, and maximum weight |
| `Weight` | Numeric weight value with unit of measurement |
| `Dimensions` | Combined length, width, height, and girth |
| `Length` | Length measurement with unit |
| `Width` | Width measurement with unit |
| `Height` | Height measurement with unit |
| `Girth` | Girth measurement with unit (relevant for non-machinable parcels) |
| `Distance` | Distance value used in post office proximity searches |

### Mail Class Types

| Type | Description |
|------|-------------|
| `MailClass` | Enum of all USPS mail classes (Priority, Ground Advantage, First Class, etc.) |
| `FirstClass` | First-Class mail parameters and weight limits |
| `Priority` | Priority Mail parameters and typical delivery days |
| `PriorityExpress` | Priority Mail Express with guaranteed delivery metadata |
| `Media` | Media Mail eligibility and weight limits |
| `Ground` | USPS Ground Advantage parameters |
| `BulkMail` | Marketing Mail / bulk mail permit information |
| `BPM` | Bound Printed Matter class parameters |
| `Library` | Library Mail class parameters |
| `Express` | Express service with scheduled delivery and pickup times |

### Pricing Types

| Type | Description |
|------|-------------|
| `PriceType` | Enum: RETAIL, CONTRACT, COMMERCIAL, COMMERCIAL_PLUS, NSA |
| `Price` | SKU-level price with effective dates and associated extra services |
| `PriceDetail` | Full price breakdown: postage, fees, extra services, and total |
| `Fee` | Individual fee with name, SKU, and price |
| `ExtraService` | Add-on service with code, name, and price |
| `InsuredMail` | Insured mail extra service with insured value and indemnity limit |
| `SignatureConfirmation` | Signature Confirmation with adult signature option |
| `CertifiedMail` | Certified Mail with electronic return receipt options |

### Label and Shipment Types

| Type | Description |
|------|-------------|
| `Shipment` | Complete shipment record linking addresses, package, label, and price |
| `Label` | Generated shipping label with tracking number, image, and format |
| `LabelFormat` | Enum: PDF, TIFF, SVG, PNG, ZPL203DPI, ZPL300DPI, PAPERLESS |
| `Barcode` | Barcode image parameters for label rendering |
| `ReturnLabel` | Return shipping label linked to an original shipment |
| `Returns` | Return shipment record with return tracking and type |
| `ShipFromUSPS` | Ship From USPS carrier pickup service record |
| `OpenDistribute` | Open and Distribute service code |
| `IMpb` | Intelligent Mail Package Barcode value and type |
| `IMb` | Intelligent Mail Barcode with routing code and service type |
| `POBox` | PO Box details including pricing and location |

### Pickup Types

| Type | Description |
|------|-------------|
| `PickupAvailability` | Available pickup dates and window for a given address |
| `PickupSchedule` | Scheduled pickup confirmation with estimated time |
| `PickupConfirmation` | Confirmed pickup with confirmation number and status |
| `PickupLocationPreferences` | Location hint and special instructions for a pickup |

### Post Office Types

| Type | Description |
|------|-------------|
| `PostOffice` | Post office facility with address, hours, services, and distance |
| `POLocations` | Collection of post office results from a proximity search |
| `PODays` | Full weekly hours schedule for a post office |
| `POHours` | Open/close times or closed flag for a single day |

### Service Standards Types

| Type | Description |
|------|-------------|
| `ServiceStandards` | Delivery day range for a mail class between two ZIP codes |
| `StandardDays` | Min/max delivery day count |
| `StandardDate` | Scheduled delivery date with acceptance cutoff |

### Utility Types

| Type | Description |
|------|-------------|
| `Alert` | Error, warning, or informational message returned by API operations |
| `AlertType` | Enum: ERROR, WARNING, INFO |

## Root Operations

### Queries

- `validateAddress` — validate and standardize a US address
- `lookupZipCode` — retrieve full details for a ZIP code
- `lookupCityState` — resolve city and state from a ZIP code
- `lookupZipCodes` — find ZIP codes for a city and state
- `trackPackage` — retrieve tracking summary for a single tracking number
- `trackPackages` — retrieve tracking summaries for multiple tracking numbers
- `getDomesticPrices` — get pricing for a given origin, destination, package, and mail class
- `getExtraServices` — list available extra services for a mail class
- `checkPickupAvailability` — check if carrier pickup is available at an address
- `findPostOffices` — locate nearby post offices by ZIP code and radius
- `getServiceStandards` — get expected delivery days between two ZIP codes
- `getLabel` — retrieve a previously created label by ID
- `getPOBox` — list PO Box options for a ZIP code

### Mutations

- `requestToken` — exchange client credentials for an OAuth 2.0 bearer token
- `createLabel` — create a domestic shipping label
- `cancelLabel` — cancel a shipping label by tracking number
- `createReturnLabel` — generate a return shipping label
- `schedulePickup` — schedule a carrier pickup at an address
- `updatePickup` — modify an existing pickup reservation
- `cancelPickup` — cancel a scheduled pickup

## References

- Developer Portal: [https://developer.usps.com/](https://developer.usps.com/)
- Getting Started: [https://developers.usps.com/getting-started](https://developers.usps.com/getting-started)
- GitHub Examples: [https://github.com/USPS/api-examples](https://github.com/USPS/api-examples)
- Addresses API: [https://developers.usps.com/addressesv3](https://developers.usps.com/addressesv3)
- Tracking API: [https://developers.usps.com/trackingv3](https://developers.usps.com/trackingv3)
- Labels API: [https://developers.usps.com/labelsv3](https://developers.usps.com/labelsv3)
- Prices API: [https://developers.usps.com/pricesv3](https://developers.usps.com/pricesv3)
- OAuth 2.0: [https://developers.usps.com/Oauth](https://developers.usps.com/Oauth)
