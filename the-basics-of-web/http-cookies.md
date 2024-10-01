# HTTP Cookies

**HTTP cookies** are small pieces of data that are sent from a web server to a user's browser and stored on the user’s device. They are widely used in web development to remember information about users, enhance their browsing experience, and enable essential website functionalities, such as session management, personalization, and tracking.

{% hint style="info" %}
Remember HTTP is a stateless protocol and hence does not know about previous interactions from the same client.
{% endhint %}

Cookies can be restricted to specific domains and paths, allowing them to be valid only on certain pages or subdomains:

```bash
Set-Cookie: key=anyvalue; domain=example.com; Path=/search/
```

{% hint style="warning" %}
When setting a cookie with`domain=example.com`, it will be accessible to all subdomains like `shop.example.com` and `blog.example.com`. To restrict access to a specific subdomain, set the cookie with `domain=sub.example.com`.&#x20;
{% endhint %}

## Cookie Attributes

When working with cookies in web development, it's essential to understand certain attributes that control their behavior and security.

### 1. Domain

The **Domain** attribute specifies which domain(s) can access the cookie. By default, cookies are only accessible to the domain that set them. However, you can explicitly set the domain to allow subdomains to access the cookie.

This cookie will be accessible to `example.com` and all its subdomains, such as `sub.example.com:`

```bash
Set-Cookie: userID=123; Domain=example.com
```

### 2. Path

The **Path** attribute defines the URL path that must exist in the requested URL for the cookie to be sent. This allows you to restrict the cookie to specific sections of your website.

This cookie will only be sent to the server when requests are made to the `/shop` path or any subdirectories:

```bash
Set-Cookie: cartID=456; Path=/shop
```

### 3. Max-Age

The **Max-Age** attribute defines the lifetime of a cookie in **seconds**. Once the specified time expires, the browser automatically deletes the cookie. This attribute is useful when you want to set an expiration time for your cookie to control how long it remains valid.

In this example, the `sessionID` cookie will expire after **3600 seconds** (or 1 hour):

```bash
Set-Cookie: sessionID=abcF4bc2_dsx13; Max-Age=3600
```

### 4. HttpOnly

The **HttpOnly** attribute is a security feature that prevents JavaScript from accessing the cookie via the `document.cookie` API. This is crucial in defending against **Cross-Site Scripting (XSS)** attacks, where malicious scripts attempt to steal cookies.

Example:

```bash
Set-Cookie: sessionID=abcF4bc2_dsx13; HttpOnly
```

### 5. Secure

The **Secure** attribute ensures that the cookie is transmitted only over **HTTPS** connections, protecting it from being intercepted during transit. Cookies marked as `Secure` will not be sent over unencrypted HTTP connections, making them safer on public or untrusted networks.

Example:

```bash
Set-Cookie: sessionID=abcF4bc2_dsx13; Secure
```

### 6. Expires

The **Expires** attribute specifies the exact date and time when the cookie will be deleted. It is similar to `Max-Age`, but instead of specifying the lifespan in seconds, `Expires` sets a specific point in time when the cookie becomes invalid.

Example:

```bash
Set-Cookie: sessionID=abcF4bc2_dsx13; Expires=Wed, 21 Oct 2025 07:28:00 GMT
```

### 7. SameSite

The **SameSite** attribute is a security feature that restricts how cookies are sent with cross-site requests, helping to prevent **Cross-Site Request Forgery (CSRF)** attacks. It has three possible values:

* **Strict**: The cookie is sent only if the request originates from the same domain as the cookie.
* **Lax**: The cookie is sent for same-site requests and when a user navigates to the site via a link from another domain, but not for cross-site requests like forms or API calls.
* **None**: The cookie is sent with all requests, regardless of origin, but must be used with the `Secure` attribute to ensure it’s only sent over HTTPS.

Example:

```bash
Set-Cookie: sessionID=abcF4bc2_dsx13; SameSite=Lax
```

### 8. Priority

The **Priority** attribute allows developers to indicate the priority of cookies when multiple cookies compete for space in the browser's cookie storage. This is particularly useful when dealing with limited storage space on clients and deciding which cookies should be retained or purged.

It has three levels:

* **High**: Essential cookies that should never be deleted before lower-priority cookies.
* **Medium**: Default priority level for cookies.
* **Low**: Non-essential cookies that can be discarded first when storage is limited.

Example:

```bash
Set-Cookie: trackingID=xyz; Priority=Low
```

