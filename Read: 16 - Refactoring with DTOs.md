# Refactoring With DTO's

Data Transfer Object (DTO) is an object that defines how the data will be sent over the network.

It is usually an instance of a POCO (plain old CLR object) class used as a container to encapsulate data and pass it from one layer of the application to another. You would typically find DTOs being used in the service layer to return data back to the presentation layer. The biggest advantage of using DTOs is decoupling clients from your internal data structures.

## DTO's help us do this:
- Remove circular references.
- Hide particular properties that clients are not supposed to view.
- Omit some properties in order to reduce payload size.
- Flatten object graphs that contain nested objects, to make them more convenient for clients.
- Avoid "over-posting" vulnerabilities.
- Decouple your service layer from your database layer.

## Why use Data Transfer Objects (DTOs)?

 If we're using models to pass data between the layers and sending data back to the presentation layer, then you’re exposing the internal data structures of your application.
 By decoupling the layers DTOs make life easier when you’re implementing APIs, MVC applications, and also messaging patterns such as Message Broker.


 You can take advantage of DTOs to abstract the domain objects of your application from the user interface or the presentation layer.

 Using DTOs you can return only the data requested and by that we hide the data.

 Data Transfer Objects typically don’t contain any business logic, they only contain data. Immutability is a desired feature when working with DTOs.

 ## How to create DTO's

 1)In the Models folder, add two DTO classes: one of them to hold all the properties and the other has some of these properties

2) Replace the two GET methods in the Controller class, with versions that return DTOs. We'll use the LINQ Select statement.

3) Modify the Post method to return a DTO.





