Here's a sample README for your URL shortener project:

---

# URL Shortener

This is a simple URL shortener application. It allows users to shorten long URLs and retrieve the shortened URL using a unique short ID.

## Features:
- **POST /url**: Accepts a URL to shorten and returns a unique short ID.
- **GET /:shortId**: Redirects to the original URL using the short ID.

## Getting Started

### Prerequisites:
- Node.js installed on your machine.

### Installation:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd url-shortener
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the application:
   ```bash
   npm run dev
   ```

   The application will run on `localhost:3000`.

### API Usage:

#### 1. POST /url
- **Endpoint**: `http://localhost:3000/url`
- **Method**: POST
- **Body**: JSON
  ```json
  {
    "url": "any_url"
  }
  ```
- **Response**: 
  ```json
  {
    "shortId": "unique_short_id"
  }
  ```

#### 2. GET /:shortId
- **Endpoint**: `http://localhost:3000/:shortId`
- **Method**: GET
- **Response**: Redirects to the original URL associated with the `shortId`.

### Testing the API with Postman:
1. Open Postman.
2. Select **POST** method and enter the URL: `http://localhost:3000/url`.
3. In the "Body" tab, select **raw** and then **JSON**.
4. Enter the following JSON:
   ```json
   {
     "url": "any_url"
   }
   ```
5. Click **Send** to get the `shortId`.
6. Use the returned `shortId` by visiting `http://localhost:3000/:shortId` in your browser to be redirected to the original URL.

---

