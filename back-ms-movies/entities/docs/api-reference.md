# API Reference

## OpenAPI Specification

The complete API specification is available in the OpenAPI format. This specification includes:

- All available endpoints
- Request/response schemas
- Authentication requirements
- Error codes and responses

## Key Endpoints

### Movies Management
- `GET /api/movies` - List all movies
- `POST /api/movies` - Create a new movie
- `GET /api/movies/{id}` - Get movie details
- `PUT /api/movies/{id}` - Update movie information
- `DELETE /api/movies/{id}` - Remove movie from catalog

### Rental Operations
- `POST /api/rentals` - Create a new rental
- `GET /api/rentals/{id}` - Get rental details
- `PUT /api/rentals/{id}/return` - Process movie return
- `GET /api/users/{userId}/rentals` - Get user rental history

### Inventory Management
- `GET /api/movies/{id}/availability` - Check movie availability
- `PUT /api/movies/{id}/inventory` - Update inventory count

For complete details, refer to the OpenAPI specification file.