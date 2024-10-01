# HTTP Response Codes

HTTP Response Codes are three-digit status codes returned by a web server in response to an HTTP request. They indicate whether the request was successful or encountered issues. These codes are categorized into five classes:

| Code Range | Category      | Description                                                                                          |
| ---------- | ------------- | ---------------------------------------------------------------------------------------------------- |
| 1xx        | Informational | Used to indicate a server is changing protocols, such as HTTP to WebSocket                           |
| 2xx        | Success       | Indicating that the request has been understood correctly                                            |
| 3xx        | Redirection   | Signifying that further action is required to complete the request, such as redirecting to a new URL |
| 4xx        | Client Error  | Indicates that the request contains incorrect or inaccurate information                              |
| 5xx        | Server Error  | Indicates that the request has encountered an issue processing the request                           |

Listed below are some of the most common ones to see:

* **200 OK**: The request has succeeded. This is the standard response for successful HTTP request.
* **201 Created**: The request has been fullfilled, resulting in the creation of a new resource.
* **204 No Content**: The server successfully processed the request, but there is no content to send in the response.
* **206 Partial Content**: The server is delivering only part of the resource due to a range header sent by the client.
* 301 Moved Permanently: The requested resource has been permanently moved to a new URL.&#x20;
* **302 Found**: The requested resource resides temporarily at a different URL.
* **400 Bad Request**: The server could not understand the request due to invalid syntax.&#x20;
* **401 Unauthorized**: The client must authenticate itself to get the requested response (usually requires login).&#x20;
* **403 Forbidden**: The server understands the request but refuses to authorize it.&#x20;
* **404 Not Found**: The server cannot find the requested resource (often returned when the URL is incorrect).&#x20;
* **405 Method Not Allowed**: The request method is known by the server but is not supported for the resource.
* **429 Too Many Requests**: The user has sent too many requests in a given amount of time ("_rate limiting_")
* **500 Internal Server Error**: The server encountered an unexpected condition that prevented it from fulfilling the request.&#x20;
* **501 Not Implemented**: The server does not support the functionality required to fulfill the request.&#x20;
* **502 Bad Gateway**: The server received an invalid response from an upstream server while acting as a gateway.&#x20;
* **503 Service Unavailable**: The server is not ready to handle the request. Common causes are server overload or maintenance.&#x20;
* **504 Gateway Timeout**: The server, while acting as a gateway, did not receive a timely response from an upstream server.&#x20;
* **505 HTTP Version Not Supported**: The server does not support the HTTP protocol version used in the request.
