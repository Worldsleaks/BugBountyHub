# HTML encoding

HTML encoding is the process of converting special characters into a format that web browsers can safely display as text, rather than interpreting them as part of the HTML structure. It's an essential technique in web security to prevent user input from being executed as code, which is particularly important for avoiding vulnerabilities like Cross-Site Scripting (XSS).

As per HTML specification, all characters references must start with an ampersand (`&`) sign, this can be followed by multiple variations such as decimal and hexadecimal encoding.

Here are various ways to represent these characters:

<table><thead><tr><th width="148">Character</th><th width="150">Named Entity</th><th>Decimal Encoding</th><th>Hexadecimal Encoding</th></tr></thead><tbody><tr><td><code>&#x3C;</code></td><td><code>&#x26;lt;</code></td><td><code>&#x26;#60;</code></td><td><code>&#x26;#X3C;</code></td></tr><tr><td><code>></code></td><td><code>&#x26;gt;</code></td><td><code>&#x26;#62;</code></td><td><code>&#x26;#X3e;</code></td></tr><tr><td><code>'</code></td><td><code>&#x26;apos;</code></td><td><code>&#x26;#39;</code></td><td><code>&#x26;#X27;</code></td></tr><tr><td><code>"</code></td><td><code>&#x26;quot;</code></td><td><code>&#x26;#34;</code></td><td><code>&#x26;#X22;</code></td></tr></tbody></table>

References:

* W3C - HTML Encoding: [https://www.w3schools.com/Html/html\_charset.asp](https://www.w3schools.com/Html/html\_charset.asp)
