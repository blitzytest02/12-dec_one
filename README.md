# 12-dec_one

A Node.js Express.js tutorial server demonstrating basic HTTP endpoint creation with Hello World and Good Evening responses.

## Description

This is a beginner-friendly tutorial project that demonstrates how to create a simple Node.js server using the Express.js framework. The server exposes two HTTP GET endpoints that return plain text responses.

## Prerequisites

Before running this project, ensure you have the following installed:

- **Node.js**: v18.x or higher (v20.x LTS recommended)
- **npm**: v9.x or higher (comes with Node.js)

To verify your installation:

```bash
node --version    # Should output v18.x.x or higher
npm --version     # Should output 9.x.x or higher
```

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd 12-dec_one
```

2. Install dependencies:

```bash
npm install
```

## Usage

Start the server using one of the following commands:

```bash
# Using npm start script
npm start

# Or directly with Node.js
node index.js
```

The server will start and display:

```
Server running on port 3000
```

## API Reference

### Endpoints

| Method | Path | Description | Response |
|--------|------|-------------|----------|
| GET | `/hello` | Returns a greeting message | `Hello world` |
| GET | `/evening` | Returns an evening greeting | `Good evening` |

### GET /hello

Returns a simple "Hello world" greeting.

**Request:**
```bash
curl http://localhost:3000/hello
```

**Response:**
- Status: `200 OK`
- Content-Type: `text/plain; charset=utf-8`
- Body: `Hello world`

### GET /evening

Returns a "Good evening" greeting.

**Request:**
```bash
curl http://localhost:3000/evening
```

**Response:**
- Status: `200 OK`
- Content-Type: `text/plain; charset=utf-8`
- Body: `Good evening`

### Error Handling

Requests to undefined routes will receive a 404 response:

```bash
curl http://localhost:3000/invalid
# Returns: 404 Not Found
```

## Testing

You can manually test the endpoints using curl or a web browser:

```bash
# Test Hello endpoint
curl http://localhost:3000/hello
# Expected output: Hello world

# Test Evening endpoint
curl http://localhost:3000/evening
# Expected output: Good evening

# Check HTTP status code
curl -I http://localhost:3000/hello
# Expected: HTTP/1.1 200 OK
```

## Project Structure

```
12-dec_one/
├── index.js          # Main application file with Express server
├── package.json      # npm project manifest
├── package-lock.json # Dependency lock file
├── node_modules/     # Installed dependencies
└── README.md         # Project documentation
```

## Dependencies

- **express** (^4.21.0): Fast, unopinionated, minimalist web framework for Node.js

## License

ISC
