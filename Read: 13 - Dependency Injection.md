# Dependency Injection

ASP.NET Core supports the dependency injection (DI) software design pattern, which is a technique for achieving Inversion of Control (IoC) between classes and their dependencies.

A dependency is an object that another object depends on.

### Dependency injection addresses these problems through:

- The use of an interface or base class to abstract the dependency implementation.
- Registration of the dependency in a service container. ASP.NET Core provides a built-in service container, IServiceProvider. Services are - typically registered in the app's Program.cs file.
- Injection of the service into the constructor of the class where it's used. The framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.

## Register groups of services with extension methods
The ASP.NET Core framework uses a convention for registering a group of related services. The convention is to use a single Add{GROUP_NAME} extension method to register all of the services required by a framework feature. 

## Design services for dependency injection
When designing services for dependency injection:

- Avoid stateful, static classes and members. Avoid creating global state by designing apps to use singleton services instead.
- Avoid direct instantiation of dependent classes within services. Direct instantiation couples the code to a particular implementation.
- Make services small, well-factored, and easily tested.
- If a class has a lot of injected dependencies, it might be a sign that the class has too many responsibilities and violates the Single Responsibility Principle (SRP). Attempt to refactor the class by moving some of its responsibilities into new classes.

## The Repository pattern
Repositories are classes or components that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer.

The Repository pattern is a well-documented way of working with a data source. 

## Single Responsibility Principle
The Single Responsibility Principal (SRP) is the idea that every method or class in your application should have exactly one reason to change. You can logically extend that to say that every class or method in your application should have exactly one (a single) job or responsibility. The short way of saying this is that each method and each class should be responsible for one, and only one task.

## Open/Close Principle

OCP states that software, be it a method or a class, should be open for extension, but closed to modification. 

## The Liskov Substitution Principle
The Liskov Substitution Principle (LSP) states that an object in your application should be able to be replaced with a type derived from it without breaking the application, Subclasses should be substitutable for their base classes

## The Interface Segregation Principle
The Interface Segregation Principle states that clients should not be forced to rely on interfaces they do not use.

## The Dependency Inversion Principle
The DIP is the idea that code should depend on abstractions; not concrete implementations. Furthermore, those abstractions should not depend on the details; the details should depend on the abstractions. 

## 