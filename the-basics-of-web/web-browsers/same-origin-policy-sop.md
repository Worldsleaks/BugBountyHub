# Same-Origin Policy (SOP)

The **Same-Origin Policy (SOP)** is a critical security mechanism implemented in web browsers to prevent malicious interactions between resources from different origins.

An origin is defined by the combination of a webpage's **protocol**, **domain** and **port:**

```bash
Origin:
http://example.com:443

http -> Scheme
example.com -> Hostname
443 -> Port
```

Example of a SOP violation:

<figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p>SOP violation</p></figcaption></figure>

Rules for interactions between different origins:

<table data-full-width="false"><thead><tr><th>Origin 1</th><th>Origin 2</th><th>Same Origin</th></tr></thead><tbody><tr><td>http://store.example.com/page.html</td><td>http://store.example.com/newpage.html</td><td>YES</td></tr><tr><td>http://store.example.com/page.html</td><td>http://news.example.com/page.html</td><td>NO</td></tr><tr><td>http://store.example.com:80/page.html</td><td>http://store.example.com:8080/page.html</td><td>NO</td></tr><tr><td>https://store.example.com:8443/page.html</td><td>ABOUT:BLANK</td><td>YES</td></tr><tr><td>https://storage.example.com/dir/page.html</td><td>https://storage.example.com/dir/subdir/page.html</td><td>YES</td></tr></tbody></table>

{% hint style="info" %}
In the table, `storage.example.com` and `about:blank` are shown on the same origin.&#x20;

`About:blank` has no origin and inherits the origin of the document that created it.
{% endhint %}
