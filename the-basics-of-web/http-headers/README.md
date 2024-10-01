# HTTP Headers

HTTP headers are key components of HTTP requests and responses that provide important information between the client (usually a browser) and the server. Headers can control security, caching, content type, and much more. Below are the most common HTTP headers you should be familiar with, particularly in the context of web security.

## 1. Host

Specifies the domain name of the server that is handling the request.

Example:&#x20;

```bash
Host: www.example.com
```

## 2. User-Agent

Identifies the client's browser or software making the request.

Example:

```bash
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64, x64)
```

## 3. Content-Type

Indicates the media type of the resource being sent, such as text, images, JSON or HTML. Tells the server or client how to interpret the body of the HTTP request or response.

Example:

```bash
Content-Type: application/json
```

## 4. Accept

Informs the server what content types the client can understand. Tells the server to send a response in a specific format that the client prefers (such as JSON, HTML, or XML).

Example:

```bash
Accept: application/json
```

## 5. Content-Length

Indicates the size (in bytes) of the body content in a request or response. Helps the client or server understand how much data is being sent and manage the connection accordingly. This can prevent truncation of data or loading failures.

Example:

```bash
Content-Length: 348
```

## 6. Set-Cookie

Sends cookies from the server to the client. Cookies are small pieces of data used to track sessions, authentication, or preferences.&#x20;

Critical for session management, user authentication, and security. The `HttpOnly` flag helps protect cookies from client-side scripts, while the `Secure` flag ensures the cookie is only transmitted over HTTPS.

Example:

```bash
Set-Cookie: sessionId=abc123; HttpOnly; Secure
```

## 7. Referer

Indicates the URL of the page that made the request. Used for analytics, logging, and sometimes security to determine the origin of a request. However, it can expose sensitive information if not handled carefully.

Example:

```bash
Referer: https://origin.example.com
```

## 8. Connection

Controls whether the network connection stays open or closes after the current request/response is completed.

Example:

```bash
Connection: keep-alive
```

## 9. X-Frame-Options

Helps prevent clickjacking attacks by controlling whether a page can be displayed in an iframe. Ensures that the website cannot be embedded in an iframe on another domain, protecting users from malicious overlays.

Example:

```bash
X-Frame-Options: DENY
```

## 10. Strict-Transport-Security (HSTS)

Instructs browsers to only communicate with the server over HTTPS, even if the user tries to access the site using HTTP. Enhances security by ensuring that all future requests to the site use HTTPS, reducing the risk of man-in-the-middle attacks.

Example:

```bash
Strict-Transport-Security: max-age=315360000; includeSubDomains
```

## 11. Content-Security-Policy (CSP)

Provides rules for what types of content (like scripts or styles) the browser is allowed to load and from which sources. Prevents **XSS (Cross-Site Scripting)** and other injection attacks by limiting what resources the browser can execute or display.

Example:

```bash
Content-Security-Policy: default-src 'self'; script-src 'self' https://trusted-source.com
```

## 12. Expires

Sets an expiration date/time after which the content should no longer be considered fresh. Controls how long a resource (like a CSS file or an image) should be cached by the browser, improving performance and reducing server load.

Example:

```bash
Expires: Wed, 21 Oct 2023 07:28:00 GMT
```
