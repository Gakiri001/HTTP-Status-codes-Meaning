<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [HTTP response status codes](#http-response-status-codes)
  - [Information responses](#information-responses)
  - [Successful responses](#successful-responses)
  - [Redirection messages](#redirection-messages)
  - [Client error responses](#client-error-responses)
  - [Server error responses](#server-error-responses)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# HTTP response status codes

1. Informational Responses (100 – 199)
1. Successful Responses (200 – 299)
1. Redirection Messages (300 – 399)
1. Client Error Responses (400 – 499)
1. Server Error Responses (500 – 599)

## Information responses
1. **100 Continue:**  
    - The client should continue with its request as the initial part has been received.  
1. **101 Switching Protocols:**  
    - The server is switching to the protocol specified in the client's Upgrade request header.
1. **102 Processing (WebDAV):**  
    - The server has received and is processing the request, but no response is available yet.
1. **103 Early Hints:**  
    - The server is suggesting resources for the client to preload while preparing the final response.

## Successful responses

1. **200 OK**:
   - The request succeeded, with different outcomes depending on the HTTP method used.

1. **201 Created**:
   - The request succeeded, and a new resource was created, typically in response to POST or PUT requests.

1. **202 Accepted**:
   - The request has been received but not yet acted upon, intended for asynchronous processing by another server or process.

1. **203 Non-Authoritative Information**:
   - The returned metadata is from a local or third-party copy, not the origin server, and is mostly used for mirrors or backups.

1. **204 No Content**:
   - There is no content to send, but the headers may be useful, and the client may update its cached headers.

1. **205 Reset Content**:
   - The server tells the client to reset the document that sent this request.

1. **206 Partial Content**:
   - This is used when the client sends a Range header to request only part of a resource.

1. **207 Multi-Status (WebDAV)**:
   - Conveys information about multiple resources, indicating multiple status codes may be appropriate.

1. **208 Already Reported (WebDAV)**:
   - Used to avoid repeatedly enumerating the internal members of multiple bindings to the same collection.

1. **226 IM Used (HTTP Delta encoding)**:
    - The server fulfilled a GET request with a representation of one or more instance-manipulations applied to the current instance.

## Redirection messages

1. **300 Multiple Choices**:
   - The request has multiple possible responses, and the user or user agent should choose one.

1. **301 Moved Permanently**:
   - The requested resource has been permanently moved to a new URL provided in the response.

1. **302 Found**:
   - The requested resource is temporarily located at a different URI, which might change in the future.

1. **303 See Other**:
   - The server directs the client to retrieve the requested resource at another URI using a GET request.

1. **304 Not Modified**:
   - Indicates that the resource has not been modified and the client can use the cached version.

1. **305 Use Proxy (Deprecated)**:
   - Previously indicated that a requested response must be accessed via a proxy, now deprecated due to security concerns.

1. **306 Unused**:
   - This code is no longer in use and is reserved.

1. **307 Temporary Redirect**:
   - The requested resource is temporarily located at another URI, and the same HTTP method must be used for the subsequent request.

1. **308 Permanent Redirect**:
   - The requested resource has been permanently moved to another URI, and the same HTTP method must be used for subsequent requests.

## Client error responses
1. **400 Bad Request**:
   - The server cannot process the request due to a client error, such as malformed syntax or deceptive request routing.
1. **401 Unauthorized**:
   - The client must authenticate itself to get the requested response.

1. **402 Payment Required (Experimental)**:
   - Reserved for future use, intended for digital payment systems but rarely used.

1. **403 Forbidden**:
   - The client does not have access rights to the content; the server is refusing the request.

1. **404 Not Found**:
   - The server cannot find the requested resource, commonly occurring on the web.

1. **405 Method Not Allowed**:
   - The request method is known by the server but not supported by the target resource.

1. **406 Not Acceptable**:
   - The server cannot find any content that conforms to the client’s criteria.

1. **407 Proxy Authentication Required**:
   - Authentication is needed to be done by a proxy.

1. **408 Request Timeout**:
   - The server would like to shut down the unused connection.

1. **409 Conflict**:
    - The request conflicts with the current state of the server.

1. **410 Gone**:
    - The requested content has been permanently deleted from the server.

1. **411 Length Required**:
    - The server rejected the request because the Content-Length header field is not defined.

1. **412 Precondition Failed**:
    - The client’s preconditions in its headers are not met by the server.

1. **413 Payload Too Large**:
    - The request entity is larger than the server is willing to process.

1. **414 URI Too Long**:
    - The requested URI is longer than the server is willing to interpret.

1. **415 Unsupported Media Type**:
    - The media format of the requested data is not supported by the server.

1. **416 Range Not Satisfiable**:
    - The specified range cannot be fulfilled; it is outside the target URI's data size.

1. **417 Expectation Failed**:
    - The expectation indicated by the Expect request header field cannot be met by the server.

1. **418 I'm a teapot**:
    - The server refuses to brew coffee with a teapot.

1. **421 Misdirected Request**:
    - The request was directed at a server that cannot produce a response.

1. **422 Unprocessable Content (WebDAV)**:
    - The request is well-formed but has semantic errors.

1. **423 Locked (WebDAV)**:
    - The resource being accessed is locked.

1. **424 Failed Dependency (WebDAV)**:
    - The request failed due to a failure of a previous request.

1. **425 Too Early (Experimental)**:
    - The server is unwilling to process a request that might be replayed.

1. **426 Upgrade Required**:
    - The server refuses to perform the request with the current protocol but might with an upgrade.

1. **428 Precondition Required**:
    - The origin server requires the request to be conditional to prevent conflicts.

1. **429 Too Many Requests**:
    - The user has sent too many requests in a given time frame.

1. **431 Request Header Fields Too Large**:
    - The server is unwilling to process the request due to large header fields.

1. **451 Unavailable For Legal Reasons**:
    - The user requested a resource that cannot legally be provided.

## Server error responses
1. **500 Internal Server Error**:
   - The server encountered an unexpected situation that it cannot handle.

1. **501 Not Implemented**:
   - The server does not support the request method and cannot process it.

1. **502 Bad Gateway**:
   - The server, while acting as a gateway, received an invalid response.

1. **503 Service Unavailable**:
   - The server is temporarily unable to handle the request, often due to maintenance or overload.

1. **504 Gateway Timeout**:
   - The server, acting as a gateway, did not receive a timely response.

1. **505 HTTP Version Not Supported**:
   - The server does not support the HTTP version used in the request.

1. **506 Variant Also Negotiates**:
   - The server has a configuration error involving transparent content negotiation.

1. **507 Insufficient Storage (WebDAV)**:
   - The server cannot store the representation needed to complete the request.

1. **508 Loop Detected (WebDAV)**:
   - The server detected an infinite loop while processing the request.

1. **510 Not Extended**:
    - Further extensions to the request are required for the server to fulfill it.

1. **511 Network Authentication Required**:
    - The client must authenticate to gain network access.