# HTTP Methods

HTTP methods are the actions that define what kind of operation the client wants to perform on the server. Each HTTP method tells the server what kind of operation the client is requesting, such as retrieving data, sending data, updating resources, or deleting them.

Common HTTP Methods:

| HTTP Method | Description                                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| GET         | Used to retrieve data from server                                                                                                    |
| POST        | Sends data to the server to create a new resource or submit data                                                                     |
| PUT         | Updates an existing resource or creates a new one if it doesn't exist                                                                |
| DELETE      | Deletes a resource from the server                                                                                                   |
| PATCH       | Partially updates a resource. Only the changes are sent, unlike PUT, which sends the full resource                                   |
| HEAD        | Retrieves the headers of a resource, similar to GET request, but without the response body                                           |
| OPTIONS     | Requests information about the communicatin options available for a specific resource, such as allowed methods or supported features |
| TRACE       | Echoes the request back to the client so that it can see any changes or alterations made by intermediate servers or proxies          |
