# Subresource Integrity Check (SIC)

**Subresource Integrity (SRI)** is a security feature that helps ensure the integrity of external resources loaded by your website, such as JavaScript files or stylesheets. It allows you to verify that the file has not been altered or tampered with after it was retrieved from a third-party source like a CDN (Content Delivery Network).

SRI works by adding a cryptographic hash to the `<script>` or `<link>` tag of the external resource. When the browser fetches the resource, it calculates its hash and compares it with the one you provided. If the hashes don’t match, the browser will block the resource from loading, preventing potentially malicious code from being executed.

Example:

```javascript
<script src="https://cdn.example.com/library.js" 
    integrity="sha384-abc123..." 
    crossorigin="anonymous">
</script>
```

{% hint style="info" %}
While CSP allows the creation of whitelists of domains to load resources, SIC prevents the loading of modified JS scripts or stylesheets.
{% endhint %}
