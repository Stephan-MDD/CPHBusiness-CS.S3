## RESTful Webservices

### Basics

* All major languages suports REST.
* REST stands for - Representational State Transfer.
* REST is an architectural style for networked hypermedia applications

### Features

* Representations
  * Multiple formats like jSON and XML.
  * Small reprensentations are advised for faster services.
  
* Messages
  * Clients send request to server, and the server replies with a response. (HTTP)
  * Theese messages contains userdata but also some metadata about the messages.

**HTTP Request**
> `<VERB>` is one of the HTTP methods like GET, PUT, POST, DELETE, OPTIONS, etc.  
> `<URI>` is the URI of the resource on which the operation is going to be performed.  
> `<HTTP Version>` is the version of HTTP, generally "HTTP v1.1".  
> `<Request Header>` contains the metadata as a collection of key-value pairs of headers and their values.  
> `<Request Body>` is the actual message content.  

**A sample POST request**
```xml
POST http://MyService/Person/
Host: MyService
Content-Type: text/xml; charset=utf-8
Content-Length: 123
<?xml version="1.0" encoding="utf-8"?>
<Person>
  <ID>1</ID>
  <Name>M Vaqqas</Name>
  <Email>m.vaqqas@gmail.com</Email>
  <Country>India</Country>
</Person>
```

**A sample GET request**
```xml
GET http://www.w3.org/Protocols/rfc2616/rfc2616.html HTTP/1.1
Host: www.w3.org
Accept: text/html,application/xhtml+xml,application/xml; …
User-Agent: Mozilla/5.0 (Windows NT 6.3; WOW64) AppleWebKit/537.36 …
Accept-Encoding: gzip,deflate,sdch
Accept-Language: en-US,en;q=0.8,hi;q=0.6
```

**HTTP Response**

The server returns 

> `<Response code>` contains the status of the request. This response code is generally the 3-digit HTTP status code.  
> `<Response Header>` contains the metadata and settings about the response message.  
> `<Response Body>` contains the representation if the request was successful.  

**Response to a GET request**

```xml
HTTP/1.1 200 OK
Date: Sat, 23 Aug 2014 18:31:04 GMT
Server: Apache/2
Last-Modified: Wed, 01 Sep 2004 13:24:52 GMT
Accept-Ranges: bytes
Content-Length: 32859
Cache-Control: max-age=21600, must-revalidate
Expires: Sun, 24 Aug 2014 00:31:04 GMT
Content-Type: text/html; charset=iso-8859-1
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns='http://www.w3.org/1999/xhtml'>
<head><title>Hypertext Transfer Protocol -- HTTP/1.1</title></head>
<body>
...
```




* URIs
* Uniform interface
* Stateless
* Links between resources
* Caching
