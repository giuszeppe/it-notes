# REST API

**REST** stands for **Representational State Transfer**, and it is an architectural style for designing networked applications. A **REST API** is a set of rules and conventions for building and interacting with web services.

## Key Principles

REST APIs are characterized by several key principles:

1. **Stateless**: Each request from a client to a server must contain all the information needed to understand and process the request. The server <u>_should not_</u> store any information about the client's state between requests.

2. **Client-Server**: The client and server are separate entities that communicate through a well-defined interface enhancing for scalability and flexibility.

3. **Uniform Interface**: REST APIs have a uniform and consistent way of interacting with resources. This typically includes using HTTP methods (GET, POST, PUT, DELETE) to perform actions on resources identified by URIs (Uniform Resource Identifiers).

4. **Resource-Based**: REST APIs are centered around resources, which can be data objects, services, or entities. Each resource is identified by a unique URI.

## HTTP Methods

REST APIs use HTTP methods to perform actions on resources:

- **GET**: Retrieve data from the server.
- **POST**: Create a new resource on the server.
- **PUT**: Update an existing resource or create a new resource if it doesn't exist.
- **DELETE**: Remove a resource from the server.
- **PATCH**: Partially update a resource.
- **HEAD**: Retrieve headers of a resource without the body.
- **OPTIONS**: Retrieve information about the communication options for the resource.

## HATEOAS

^01ab4d

**HATEOAS**(Hypermedia as the engine of application state). 
With HATEOAS, a client interacts with a network application whose application servers provide information dynamically through hypermedia 

[[REST - best_practices]]
[[REST - limitations]]