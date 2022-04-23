# Routing and Navigation Properties

Routing is responsible for matching incoming HTTP requests and dispatching those requests to the app's executable endpoints.

 Endpoints are the app's units of executable request-handling code.


## Apps can configure routing using:

- Controllers
- Razor Pages
- SignalR
- gRPC Services
- Endpoint-enabled middleware such as Health Checks.
- Delegates and lambdas registered with routing.


## Routing uses a pair of middleware, registered by UseRouting and UseEndpoints:

- UseRouting adds route matching to the middleware pipeline. This middleware looks at the set of endpoints defined in the app, and selects the best match based on the request.
- UseEndpoints adds endpoint execution to the middleware pipeline. It runs the delegate associated with the selected endpoint.

## The MapGet method is used to define an endpoint. An endpoint is something that can be:

Selected, by matching the URL and HTTP method.
Executed, by running the delegate.

## Endpoint metadata

Endpoints can have extra data attached to them. This extra data is called endpoint metadata:

- The metadata can be processed by routing-aware middleware.
- The metadata can be of any .NET type.

## Routing concepts
The routing system builds on top of the middleware pipeline by adding the powerful endpoint concept. Endpoints represent units of the app's functionality that are distinct from each other in terms of routing, authorization, and any number of ASP.NET Core's systems.

An ASP.NET Core endpoint is:

- Executable: Has a RequestDelegate.
- Extensible: Has a Metadata collection.
- Selectable: Optionally, has routing information.
- Enumerable: The collection of endpoints can be listed by retrieving the EndpointDataSource from DI.

## URL matching
Is the process by which routing matches an incoming request to an endpoint.
Is based on data in the URL path and headers.
Can be extended to consider any data in the request.

When a routing middleware executes, it sets an Endpoint and route values to a request feature on the HttpContext from the current request:

Calling HttpContext.GetEndpoint gets the endpoint.
HttpRequest.RouteValues gets the collection of route values.

## Route template precedence and endpoint selection order
Route template precedence is a system that assigns each route template a value based on how specific it is. Route template precedence:

Avoids the need to adjust the order of endpoints in common cases.
Attempts to match the common-sense expectations of routing behavior.

## URL generation concepts
URL generation:

Is the process by which routing can create a URL path based on a set of route values.
Allows for a logical separation between endpoints and the URLs that access them.

## Route template reference
Tokens within {} define route parameters that are bound if the route is matched. More than one route parameter can be defined in a route segment, but route parameters must be separated by a literal value.

## Addresses
Addresses are the concept in URL generation used to bind a call into the link generator to a set of candidate endpoints.
