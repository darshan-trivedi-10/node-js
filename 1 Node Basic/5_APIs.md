## What is APIs ??
- An API, or application programming interface, is a set of rules and protocols that define how two software systems can communicate with each other. APIs allow different software systems to exchange data and functionality, enabling them to work together and perform tasks that would be difficult or impossible to accomplish independently.

- APIs can be used to access a wide range of functionality and data, including databases, cloud services, messaging systems, and more. They are an essential part of modern software development, as they allow developers to build applications that can integrate with and extend the capabilities of other systems.

- APIs are typically accessed through a set of programming instructions or libraries, which are provided by the provider of the API. These instructions allow developers to send requests to the API and receive responses, allowing them to access and manipulate the data and functionality that the API provides.

- APIs can be public or private. Public APIs are available to developers outside of the organization that provides the API, and are typically used to enable integration with other systems or to expose certain functionality to external developers. Private APIs, on the other hand, are only available to developers within the organization that provides the API, and are often used to enable communication between different systems or applications within the organization.

- Web APIs are APIs that are accessed over the internet using standard web protocols, such as HTTP or HTTPS. These types of APIs are often used to expose data or functionality to external developers.

## Diffrent Style for building web APIs

- REST (Representational State Transfer) APIs are a type of web API that use a standardized set of HTTP methods (such as GET, POST, PUT, and DELETE) to manipulate data and functionality. REST APIs are often used for web-based applications and are designed to be easy to use and scalable.

- gRPC (Google Remote Procedure Call) APIs allow developers to access functionality from a remote system as if it were a local function. This can be useful for accessing functionality from a system that is not accessible over the internet, or for simplifying the integration process by abstracting the underlying communication mechanism.

- SOAP (Simple Object Access Protocol) APIs are a type of web API that use a standardized XML-based messaging system to transmit data between systems. SOAP APIs are often used for enterprise integration and can be accessed over a variety of transport protocols, including HTTP, HTTPS, and SMTP.

## REST APIs

- A REST (Representational State Transfer) API is a web API that uses a standardized set of HTTP methods (such as GET, POST, PUT, and DELETE) to manipulate data and functionality. REST APIs are designed to be easy to use and scalable, and they are often used for web-based applications.

## BEST PRACTICES TO DESIGN REST APIS
1. REST API MUST ACCEPT AND RESPOND WITH JSON
2. GO WITH ERROR STATUS CODES
3. DON’T USE VERBS IN URLS
4. USE PLURAL NOUNS TO NAME A COLLECTION
5. WELL COMPILED DOCUMENTATION
6. RETURN ERROR DETAILS IN THE RESPONSE BODY

## HTTP request methods
- There are several different HTTP request methods that can be used to make requests to a server. These methods are:

- **GET**: This is the most commonly used HTTP request method. It is used to retrieve information from a server.HEAD: This method is similar to GET, but it only retrieves the HTTP headers of a request, not the actual content. This can be useful for checking the status of a resource or getting metadata about it.

- **POST**: This method is used to send data to a server to be processed. It is often used to submit a form or upload a file.

- **PUT**: This method is used to update an existing resource on a server.

- **DELETE**: This method is used to delete a resource from a server.

- **CONNECT**: This method establishes a connection to a server through a proxy.

- **OPTIONS**: This method retrieves the HTTP methods that a server supports.

- **TRACE**: This method echoes the request back to the client, allowing it to be used for debugging purposes.

- **PATCH**: This method is used to apply partial modifications to a resource on a server.

- It is important to note that not all HTTP request methods are supported by all servers and resources. It is up to the server to decide which methods are supported and how they should be handled.

## Request Parameters
- Request parameters are values that are passed in the URL of an HTTP request. They are typically used to specify the resource or action that the request is intended for.

- For example, in the URL https://example.com/users?id=123, the id parameter is a request parameter.

## Query Parameters
- Query parameters are values that are added to the end of a URL to specify search criteria or other options for an HTTP request. They are typically used to filter or sort the results of a request.

- For example, in the URL https://example.com/users?sort=asc&limit=10, the sort and limit parameters are query parameters.

## Request Body
- A request body is the data included in an HTTP request, typically in the form of a JSON object. It is used to send additional information to the server, such as data for creating or updating a resource.

- For example, a POST request to create a new user might include a request body like this:
```js
{
  "name": "John Smith",
  "email": "john@example.com",
  "password": "abc123"
}
```
