# 12-dec_one

A simple Node.js server tutorial using Express.js framework demonstrating basic HTTP endpoint creation.

## Description

This project is an educational tutorial application that demonstrates how to build a basic HTTP server using Node.js and Express.js. The server exposes two GET endpoints that return simple text responses, making it ideal for beginners learning web server development.

**Features:**
- Express.js-based HTTP server
- Two GET endpoints (`/hello` and `/evening`)
- Simple, clean, and beginner-friendly code structure
- Minimal dependencies for easy understanding

## Prerequisites

Before running this application, ensure you have the following installed:

- **Node.js**: v18.x or v20.x LTS (recommended)
- **npm**: v8.x or higher (comes bundled with Node.js)

To verify your Node.js installation:

```bash
node --version
npm --version
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

This will install Express.js and all required dependencies.

## Usage

Start the server using one of the following commands:

```bash
npm start
```

Or directly with Node.js:

```bash
node index.js
```

The server will start and display:

```
Server running on port 3000
```

The server will be accessible at `http://localhost:3000`.

## API Reference

### GET /hello

Returns a "Hello world" greeting.

**Request:**
```
GET http://localhost:3000/hello
```

**Response:**
- **Status Code:** 200 OK
- **Content-Type:** text/plain; charset=utf-8
- **Body:** `Hello world`

### GET /evening

Returns a "Good evening" greeting.

**Request:**
```
GET http://localhost:3000/evening
```

**Response:**
- **Status Code:** 200 OK
- **Content-Type:** text/plain; charset=utf-8
- **Body:** `Good evening`

## Testing

You can verify the endpoints are working correctly using `curl` or any HTTP client.

### Using curl

Test the `/hello` endpoint:

```bash
curl http://localhost:3000/hello
```

Expected output: `Hello world`

Test the `/evening` endpoint:

```bash
curl http://localhost:3000/evening
```

Expected output: `Good evening`

### Verifying HTTP Headers

To check the response headers:

```bash
curl -I http://localhost:3000/hello
```

Expected output includes:
```
HTTP/1.1 200 OK
Content-Type: text/plain; charset=utf-8
```

### Testing Invalid Routes

Test that invalid routes return 404:

```bash
curl http://localhost:3000/invalid
```

Expected: 404 Not Found response

## ⚠️ Production Disclaimer

> **WARNING:** This tutorial application is designed for **educational purposes and local development only**. It should NOT be deployed to production without implementing:
>
> - Authentication and authorization
> - HTTPS/TLS encryption
> - Input validation and sanitization
> - Rate limiting
> - Security headers (e.g., Helmet.js)
> - Error handling middleware
> - Logging and monitoring
> - Environment-based configuration

## License

This project is provided for educational purposes.
