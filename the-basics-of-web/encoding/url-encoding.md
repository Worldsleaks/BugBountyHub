# URL encoding

URL encoding is a process used to encode special characters in URLs to ensure that they are transmitted correctly over the internet. URLs can only be sent over the internet using the ASCII character set. Certain characters in URLs have special meanings (like `?`, `&`, `#`, etc.), and spaces or other non-ASCII characters can cause problems if not handled properly. URL encoding converts these characters into a format that can be safely used in URLs.

In this example, the password contains ampersand `&` , which if not encoded will be treated as a parameter and will set `password` to `tJ` and "`MS_L`"

```bash
URL:
https://example.com/login.php?username=admin&password=tJ&MS_l

Encoded URL:
https://example.com/login.php?username=admin&password=tJ%26MS_l
```

Common characters encoded and encoded value:

| Character          | Encoded Value |
| ------------------ | ------------- |
| Space              | `%20`         |
| Double Quote (`"`) | `%22`         |
| Less Than (`<`)    | `%3C`         |
| Greater Than (`>`) | `%3E`         |
| Pound (`#`)        | `%23`         |
| Percentage (`%`)   | `%25`         |
| Ampersand (`&`)    | `%26`         |
| Slash (`/`)        | `%2F`         |
| Plus (`+`)         | `%2B`         |
| Equal (`=`)        | `%3D`         |

## Double Encoding

In double encoding, the characters are encoded twice:

* The **first level of encoding** converts the character into a percent-encoded form.
* The **second level of encoding** is appliedto the percent-encoded characters.

Example: `&` > `%26` > `%2526`

```bash
URL:
https://example.com/login.php?username=admin&password=tJ&MS_l

First encode:
https://example.com/login.php?username=admin&password=tJ%26MS_l

Second encode:
https://example.com/login.php?username=admin&password=tJ%2526MS_l
```
