# Location API

## Overview

The Location API manages user locations and geographic data with comprehensive CRUD operations and validation.

## Features

- **Address Management**: Home, work, billing, shipping addresses
- **Geographic Hierarchy**: Countries, regions, cities, neighborhoods
- **Location Types**: Categorization and validation
- **Geospatial Support**: Latitude/longitude coordinates
- **Address Validation**: Postal codes and address verification

## Key Endpoints

- `POST /api/locations` - Create new location
- `GET /api/locations` - List locations
- `GET /api/locations/{id}` - Get location details
- `PUT /api/locations/{id}` - Update location
- `DELETE /api/locations/{id}` - Remove location
- `GET /api/users/{userId}/locations` - Get user locations
- `POST /api/locations/validate` - Validate address

For complete API specification, refer to the OpenAPI documentation.