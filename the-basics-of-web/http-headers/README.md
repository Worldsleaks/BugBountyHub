# HTTP Headers

HTTP headers are key components of HTTP requests and responses that provide important information between the client (usually a browser) and the server. Headers can control security, caching, content type, and much more. Below are the most common HTTP headers you should be familiar with, particularly in the context of web security.

## 1. Host

Specifies the domain name of the server that is handling the request.

Example:&#x20;

```http
Host: www.example.com
```

## 2. User-Agent

Identifies the client's browser or software making the request.

Example:

```http
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64, x64)
```

## 3. Content-Type

Indicates the media type of the resource being sent, such as text, images, JSON or HTML. Tells the server or client how to interpret the body of the HTTP request or response.

Example:

```http
Content-Type: application/json
```

## 4. Accept

Informs the server what content types the client can understand. Tells the server to send a response in a specific format that the client prefers (such as JSON, HTML, or XML).

Example:

```http
Accept: application/json
```

## 5. Content-Length

Indicates the size (in bytes) of the body content in a request or response. Helps the client or server understand how much data is being sent and manage the connection accordingly. This can prevent truncation of data or loading failures.

Example:

```http
Content-Length: 348
```

## 6. Set-Cookie

Sends cookies from the server to the client. Cookies are small pieces of data used to track sessions, authentication, or preferences.&#x20;

Critical for session management, user authentication, and security. The `HttpOnly` flag helps protect cookies from client-side scripts, while the `Secure` flag ensures the cookie is only transmitted over HTTPS.

Example:

```http
Set-Cookie: sessionId=abc123; HttpOnly; Secure
```

## 7. Referer

Indicates the URL of the page that made the request. Used for analytics, logging, and sometimes security to determine the origin of a request. However, it can expose sensitive information if not handled carefully.

Example:

```http
Referer: https://origin.example.com
```

## 8. Connection

Controls whether the network connection stays open or closes after the current request/response is completed.

Example:

```http
Connection: keep-alive
```

## 9. X-Frame-Options

Helps prevent clickjacking attacks by controlling whether a page can be displayed in an iframe. Ensures that the website cannot be embedded in an iframe on another domain, protecting users from malicious overlays.

Example:

```http
X-Frame-Options: DENY
```

## 10. Strict-Transport-Security (HSTS)

Instructs browsers to only communicate with the server over HTTPS, even if the user tries to access the site using HTTP. Enhances security by ensuring that all future requests to the site use HTTPS, reducing the risk of man-in-the-middle attacks.

Example:

```http
Strict-Transport-Security: max-age=315360000; includeSubDomains
```

## 11. Content-Security-Policy (CSP)

Provides rules for what types of content (like scripts or styles) the browser is allowed to load and from which sources. Prevents **XSS (Cross-Site Scripting)** and other injection attacks by limiting what resources the browser can execute or display.

Example:

```http
Content-Security-Policy: default-src 'self'; script-src 'self' https://trusted-source.com
```

## 12. Expires

Sets an expiration date/time after which the content should no longer be considered fresh. Controls how long a resource (like a CSS file or an image) should be cached by the browser, improving performance and reducing server load.

Example:

```http
Expires: Wed, 21 Oct 2023 07:28:00 GMT
```

## 13. Sec-GPC

Signals that the user requests not to have their personal data sold or shared, in line with privacy regulations (like CCPA).

Example:

```http
Sec-GPC: 1    # Respect the user's privacy preferences and avoid tracking
Sec-GPC: 0    # User is not requesting any special privacy protections
```

## 14. Accept-Language

Tells the server the preferred language for the content, helping sites serve localized versions.

Example:

```http
Accept-Language: en-US,en
```

## 15. Accept-Encoding

Informs the server which compression formats the browser can handle, allowing faster page loads.

```http
Accept-Encoding: gzip, deflate, br
```

## 16. Date

Provides the **date and time** when the server generated the response, useful for caching and synchronization.

Example:

```http
Date: Fri, 04 Oct 2024 08:26:52 GMT
```

## 17. Server

Identifies the **server software** handling the request, including its version and operating system.

Example:

```http
Server: Apache/2.4.41 (Ubuntu)
```

## 18. Vary

Tells caches that the response may vary depending on the **`Accept-Encoding`** header, ensuring the correct version is delivered (compressed or uncompressed).

Example:

```http
Vary: Accept-Encoding    # Server provides different responses based on whether the client accepts compression methods
```

## 19. Allow

Indicates the **HTTP methods** that the server supports for a particular resource. This header is typically sent in response to a **405 Method Not Allowed** status or in response to an **OPTIONS** request.

Example:

```http
Allow: GET, POST, OPTIONS, HEAD
```

## 20. WWW-Authenticate

Informs the client that it needs to provide authentication credentials to access the requested resource. It is typically sent in response to an **HTTP 401 Unauthorized** status.

Example:

```http
WWW-Authenticate: Basic realm="User Login"
```

## 21. X-Original-URL

The `X-Original-URL` header is typically used in reverse proxy setups to indicate the original URL requested by the client before any modifications by the proxy. This helps the backend server understand the initial request.

```http
X-Original-URL: /admin
```

## 22. **X-Forwarded-For**

Indicates the original IP address of the client making the request through a proxy or load balancer. This header is useful for identifying the real client IP in cases where the server receives the IP of the proxy instead.

```http
X-Forwarded-For: 192.168.1.1, 203.0.113.5
```

