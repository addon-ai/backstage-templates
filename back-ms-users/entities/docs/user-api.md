# User API

## Overview

The User API provides comprehensive user account management with full CRUD operations and search capabilities.

## Features

- **User Registration**: Create new user accounts
- **Authentication**: Login and session management
- **Profile Management**: Update user information
- **User Search**: Find users with pagination
- **Account Status**: Manage active/inactive/suspended states

## Key Endpoints

- `POST /api/users` - Register new user
- `GET /api/users` - List users with pagination
- `GET /api/users/{id}` - Get user details
- `PUT /api/users/{id}` - Update user profile
- `DELETE /api/users/{id}` - Deactivate user account
- `POST /api/auth/login` - User authentication
- `GET /api/users/search` - Search users

For complete API specification, refer to the OpenAPI documentation.