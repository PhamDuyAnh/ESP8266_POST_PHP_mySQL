# ESP8266_POST_PHP_mySQL
Ví dụ mẫu dùng ESP8266 với giao thức POST hoặc GET để gửi dữ liệu đến PHP Server

## What is HTTP?
The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients and servers.

HTTP works as a request-response protocol between a client and server. Each Hypertext Transfer Protocol (HTTP) message is either a request or a response. A server listens on a connection for a request, parses each message received, interprets the message semantics in relation to the identified request target, and responds to that request with one or more response messages. A client constructs request messages to communicate specific intentions, examines received responses to see if the intentions were carried out, and determines how to interpret the results.

A web browser may be the client, and an application on a computer that hosts a web site may be the server.

### Example:
A client (browser) submits an HTTP request to the server; then the server returns a response to the client. The response contains status information about the request and may also contain the requested content.

### Two HTTP Request Methods: GET and POST
Two commonly used methods for a request-response between a client and server are: GET and POST.
- GET – Requests data from a specified resource
- POST – Submits data to be processed to a specified resource
## GET
The GET method requests transfer of a current selected representation for the target resource. GET is the primary mechanism of information retrieval and the focus of almost all performance optimizations.  Hence, when people speak of retrieving some identifiable information via HTTP, they are generally referring to making a GET request.
### The GET Method
Note that the query string (name/value pairs) is sent in the URL of a GET request:

http://url/test/demo_form.php?name1=value1&name2=value2

### Some other notes on GET requests:
- GET requests can be cached
- GET requests remain in the browser history
- GET requests can be bookmarked
- GET requests should never be used when dealing with sensitive data
- GET requests have length restrictions
- GET requests should be used only to retrieve data
## POST
The POST method requests that the target resource process the representation enclosed in the request according to the resource’s own specific semantics. For example, POST is used for the following functions (among others):
1. Providing a block of data, such as the fields entered into an HTML form, to a data-handling process;
2. Posting a message to a bulletin board, newsgroup, mailing list, blog, or similar group of articles;
3. Creating a new resource that has yet to be identified by the origin server; and
4. Appending data to a resource’s existing representation(s).
An origin server indicates response semantics by choosing an appropriate status code depending on the result of processing the POST request; almost all of the status codes defined by this specification might be received in a response to POST (the exceptions being 206 (Partial Content), 304 (Not Modified), and 416 (Range Not Satisfiable)).

### The POST Method
Note that the query string (name/value pairs) is sent in the HTTP message body of a POST request:

    POST / HTTP/1.1
    Host: foo.com
    Content-Type: application/x-www-form-urlencoded
    Content-Length: 13

    say=Hi&to=Mom
### Some other notes on POST requests:
  - POST requests are never cached
  - POST requests do not remain in the browser history
  - POST requests cannot be bookmarked
  - POST requests have no restrictions on data length
