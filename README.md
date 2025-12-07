# alx-project-0x14

This project contains the CineSeek movie application built with Next.js, TypeScript, and Tailwind CSS.

## API Overview

The MoviesDatabase API provides comprehensive access to a vast collection of movie data, including titles, release information, images, and metadata. This RESTful API allows developers to search, filter, and retrieve detailed information about movies from various years and genres. Key features include:

- Access to extensive movie database with titles, posters, and release years
- Advanced filtering capabilities by year, genre, and other criteria
- Pagination support for efficient data retrieval
- High-quality movie poster images
- Structured JSON responses for easy integration

## Version

API Version: v1 (RapidAPI MoviesDatabase)

## Available Endpoints

The main endpoints available in the MoviesDatabase API include:

- **GET /titles** - Retrieve a list of movies with optional filtering parameters
  - Query parameters: year, genre, page, limit, sort
  - Returns paginated list of movie titles with metadata
  
- **GET /titles/{id}** - Get detailed information about a specific movie
  - Returns comprehensive movie data including cast, crew, and ratings
  
- **GET /titles/search/{query}** - Search for movies by title
  - Returns matching movie results based on search query

## Request and Response Format

### Typical Request Structure

```http
GET /titles?year=2024&sort=year.decr&limit=12&page=1&genre=Action
Headers:
  x-rapidapi-host: moviesdatabase.p.rapidapi.com
  x-rapidapi-key: YOUR_API_KEY
```

### Typical Response Object

```json
{
  "page": 1,
  "next": "/titles?page=2&limit=12",
  "entries": 12,
  "results": [
    {
      "id": "tt1234567",
      "primaryImage": {
        "url": "https://example.com/poster.jpg"
      },
      "titleText": {
        "text": "Movie Title"
      },
      "releaseYear": {
        "year": 2024
      }
    }
  ]
}
```

## Authentication

Authentication is required for all API requests using RapidAPI's authentication system:

1. **API Key**: Obtain an API key from RapidAPI by subscribing to the MoviesDatabase API
2. **Required Headers**:
   - `x-rapidapi-host`: moviesdatabase.p.rapidapi.com
   - `x-rapidapi-key`: YOUR_API_KEY

Include these headers in every request to authenticate successfully.

## Error Handling

Common error responses from the API:

- **401 Unauthorized**: Invalid or missing API key
  - Solution: Verify your API key is correct and included in headers
  
- **403 Forbidden**: API quota exceeded or subscription inactive
  - Solution: Check your RapidAPI subscription status and usage limits
  
- **404 Not Found**: Requested resource does not exist
  - Solution: Verify the endpoint URL and resource ID
  
- **429 Too Many Requests**: Rate limit exceeded
  - Solution: Implement request throttling and respect rate limits
  
- **500 Internal Server Error**: Server-side error
  - Solution: Retry the request after a brief delay

Handle errors gracefully in your code by checking response status codes and providing appropriate user feedback.

## Usage Limits and Best Practices

### Usage Limits

- **Rate Limits**: Varies by subscription tier (typically 500-10,000 requests per month)
- **Request Rate**: Maximum requests per second depends on your plan
- **Data Limits**: Response size limits apply to prevent excessive data transfer

### Best Practices

1. **Caching**: Implement caching to reduce redundant API calls and improve performance
2. **Pagination**: Use pagination parameters (page, limit) to retrieve data in manageable chunks
3. **Error Handling**: Implement robust error handling for all API calls
4. **Rate Limiting**: Monitor your usage and implement request throttling if needed
5. **Efficient Queries**: Use specific filters (year, genre) to reduce response size
6. **Environment Variables**: Store API keys securely in environment variables, never in code
7. **Request Optimization**: Batch requests when possible and avoid unnecessary calls
8. **Timeout Handling**: Set appropriate timeout values for API requests
9. **Monitoring**: Track API usage to stay within quota limits