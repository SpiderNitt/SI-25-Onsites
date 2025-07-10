# URL Shortener with Hash Function

## Objective

Build a lightweight URL shortening service that generates compact, unique links using a hash function. Users can input long URLs and receive shortened versions that redirect to the original URL. An optional feature allows users to receive the shortened URL via email.

## Key Features to Implement

### 1. URL Shortening Using Hash Function

**Functionality:**  
Generate a unique, short URL identifier using a hashing mechanism.

**Requirements:**
- Accept a long URL as input.
- Use a hash function (e.g., SHA-256, MurmurHash, or Base62 encoding) to generate a short ID.
- Store the mapping between the hash and original URL in a database.
- Return a shortened URL in the format: `https://yourdomain.com/abc123`.

### 2. URL Redirection

**Functionality:**  
Redirect users to the original URL when accessing the shortened link.

**Requirements:**
- Extract short code from incoming request.
- Look up the corresponding long URL from the database.
- Perform a 301/302 redirect to the original URL.

### 3. Optional: Email Delivery of Shortened URL

**Functionality:**  
Allow users to receive their shortened URL by email.

**Requirements:**
- Add an optional email input field on the form.
- If an email is provided, send the shortened URL using an SMTP service or email API (e.g., Nodemailer, SendGrid).
- Ensure email is sent asynchronously and securely.

### 4. API Endpoints

**Functionality:**  
Provide RESTful endpoints for frontend/backend communication.

**Requirements:**
- `POST /shorten` – Accepts long URL (and optional email), returns short URL.
- `GET /:shortId` – Redirects to the original URL.
- (Optional) `GET /analytics/:shortId` – Returns metadata like usage count, timestamps.

### 5. Basic UI (Optional)

**Functionality:**  
Allow users to interact with the service via a clean frontend interface.

**Requirements:**
- Input for long URL and optional email.
- Display of shortened URL upon submission.
- Success/error notifications.

---

## Optional Enhancements

- URL expiration or usage limits.
- User login and dashboard to manage created links.
- QR code generation for shortened links.
- Rate limiting to prevent abuse.
- Custom aliases for short URLs.


