# Album API

This is a simple RESTful API built using the Go programming language and the [Gin](https://github.com/gin-gonic/gin) web framework. It provides basic CRUD operations for managing albums.

## Features
- Retrieve a list of albums
- Retrieve a specific album by ID
- Add a new album

## Prerequisites
Ensure you have the following installed before running the project:
- [Go](https://go.dev/) (1.18 or later)
- [Gin](https://github.com/gin-gonic/gin) web framework

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/album-api.git
   cd album-api
   ```
2. Install dependencies:
   ```sh
   go mod tidy
   ```

## Running the Application
To start the API server, run:
```sh
  go run main.go
```
By default, the server will run on `http://localhost:8080`.

## API Endpoints
### Get all albums
**Request:**
```http
GET /albums
```
**Response:**
```json
[
  { "id": "1", "title": "Blue Train", "artist": "John Coltrane", "price": 56.99 },
  { "id": "2", "title": "Jeru", "artist": "Gerry Mulligan", "price": 17.99 },
  { "id": "3", "title": "Sarah Vaughan and Clifford Brown", "artist": "Sarah Vaughan", "price": 39.99 }
]
```

### Get album by ID
**Request:**
```http
GET /albums/:id
```
Example:
```http
GET /albums/1
```
**Response:**
```json
{ "id": "1", "title": "Blue Train", "artist": "John Coltrane", "price": 56.99 }
```

### Add a new album
**Request:**
```http
POST /albums
Content-Type: application/json
```
Example request body:
```json
{
  "id": "4",
  "title": "Kind of Blue",
  "artist": "Miles Davis",
  "price": 29.99
}
```
**Response:**
```json
{
  "id": "4",
  "title": "Kind of Blue",
  "artist": "Miles Davis",
  "price": 29.99
}
```

## License
This project is licensed under the MIT License. See `LICENSE` for details.

## Author
Created by [Your Name](https://github.com/yourusername).

