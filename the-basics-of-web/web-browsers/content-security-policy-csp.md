# Content Security Policy (CSP)

**Content Security Policy (CSP)** is a security feature used by web developers to mitigate the risk of various types of attacks, such as **Cross-Site Scripting (XSS)**, **clickjacking**, and other code injection attacks that result from the execution of malicious content in the browser.

CSP works by allowing site administrators to specify which sources of content are trusted, thereby preventing the browser from loading or executing any resources that are not explicitly allowed.

### Key CSP Directives

To define which content can be loaded and executed, CSP uses various **directives** that provide fine-grained control over different types of resources. Each directive controls a specific type of content, allowing developers to enforce security at multiple levels. Here are the most common directives used in CSP:

* **`default-src`**: Specifies the default policy for fetching resources like scripts, styles, and images when no specific policy is set.
* **`script-src`**: Restricts the sources from which JavaScript can be loaded and executed.
* **`img-src`**: Limits where images can be loaded from.
* **`style-src`**: Controls where CSS files can be loaded from.
* **`object-src`**: Specifies allowed sources for `<object>`, `<embed>`, and `<applet>` elements.
* **`frame-ancestors`**: Specifies who is allowed to embed the site in a frame (helpful for preventing clickjacking).
* **`report-uri`**: Specifies a URL where the browser sends reports if a policy violation occurs, allowing the site administrator to track and fix issues.

### Example

This policy would ensure that only JavaScript from the specified jQuery library is executed, blocking any other scripts that are not from this source:

```bash
Content-Security-Policy:script-src http://code.jquery.com/jquery-1.11.0.min.js;
```
