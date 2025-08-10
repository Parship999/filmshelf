# Go Movies CRUD API

A simple RESTful API built with Go that implements CRUD (Create, Read, Update, Delete) operations for managing movie information. The project uses the Gorilla Mux router for handling HTTP requests.

## Features

- Get all movies
- Get a specific movie by ID
- Create a new movie
- Update an existing movie
- Delete a movie

## Project Structure

```
├── main.go     # Main application file
├── go.mod      # Go module file
└── go.sum      # Go module checksum file
```

## Prerequisites

- Go 1.16 or higher
- Gorilla Mux package

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd go-movies-crud
```

2. Install dependencies:
```bash
go mod download
```

## Running the Application

To start the server:
```bash
go run main.go
```

The server will start on `http://localhost:8000`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/movies` | Get all movies |
| GET | `/movies/{id}` | Get a specific movie |
| POST | `/movies/{id}` | Create a new movie |
| PUT | `/movies/{id}` | Update a movie |
| DELETE | `/movies/{id}` | Delete a movie |

## Data Structure

### Movie
```json
{
    "id": "string",
    "isbn": "string",
    "title": "string",
    "director": {
        "firstname": "string",
        "lastname": "string"
    }
}
```

## Example Usage

### Get All Movies
```bash
curl http://localhost:8000/movies
```

### Create a Movie
```bash
curl -X POST http://localhost:8000/movies -H "Content-Type: application/json" -d '{
    "isbn": "438227",
    "title": "New Movie",
    "director": {
        "firstname": "John",
        "lastname": "Doe"
    }
}'
```

## License

This project is open source and available under the [MIT License](LICENSE).
