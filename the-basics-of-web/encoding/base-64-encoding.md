# Base 64 encoding

Base64 encoding is a method of converting binary data (like images, files, or even scripts) into a string of ASCII characters. It is often used in web applications to safely transmit or store data that might otherwise include characters that could cause issues in certain contexts (e.g., URLs, HTTP headers, or email bodies).

Using the developers tools console:

<pre class="language-javascript"><code class="lang-javascript">Base64 encode:
<strong>>> btoa("Hello World!")
</strong>&#x3C;- "SGVsbG8gV29ybGQh" 

Base64 decode:
>> atob("SGVsbG8gV29ybGQh")
&#x3C;- "Hello World!" 
</code></pre>

Also you can always use [CyberChef ](https://gchq.github.io/CyberChef/)for encode/decode operations in other bases.
