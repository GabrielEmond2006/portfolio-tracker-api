# portfolio-tracker-api 
A lightweight, high-performance RESTful API built with C# and .NET 8 Minimal APIs to manage financial asset holdings. This standalone backend service implements modern web practices, including asynchronous operations, dependency injection, request validation, and in-memory persistence via Entity Framework Core InMemory.

## Features
- Full CRUD operations for asset holdings: create, read single, list all, update, and delete (liquidate).
- Automatic calculation of total holding values based on quantity and purchase unit price.
- Interactive API exploration and testing via integrated Swagger / OpenAPI UI.
- Standardized HTTP status codes (200 OK, 201 Created, 400 Bad Request, 404 Not Found, 204 No Content).

## Tech Stack
- **C# / .NET 8** (ASP.NET Core Minimal APIs)
- **Entity Framework Core InMemory** (Data persistence)
- **Swashbuckle / OpenAPI** (Interactive documentation)

## Getting Started

### Prerequisites
- [.NET 8 SDK](https://dotnet.microsoft.com/download) installed on your machine.

### Installation and Run
1. Clone the repository:
   git clone https://github.com/your-username/portfolio-tracker-api.git
   cd portfolio-tracker-api

2. Restore dependencies and run the application:
   dotnet run

3. Access the interactive Swagger documentation:
   Open your browser at `https://localhost:xxxx/swagger` (refer to the exact port printed in your console).

## Key Endpoints
- `GET /api/portfolio`: Retrieve all asset positions.
- `GET /api/portfolio/{id}`: Retrieve a specific asset position by ID.
- `POST /api/portfolio`: Add a new asset (ticker, quantity, purchase price).
- `PUT /api/portfolio/{id}`: Update an asset's quantity or purchase price.
- `DELETE /api/portfolio/{id}`: Remove an asset from the portfolio.
