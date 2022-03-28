## Interfaces
An interface contains definitions for a group of related functionalities that a non-abstract class or a struct must implement. An interface may define static methods, which must have an implementation.

By using interfaces, you can, for example, include behavior from multiple sources in a class. That capability is important in C# because the language doesn't support multiple inheritance of classes. 

Interfaces can contain instance methods, properties, events, indexers, or any combination of those four member types. Interfaces may contain static constructors, fields, constants, or operators.

To implement an interface member, the corresponding member of the implementing class must be public, non-static, and have the same name and signature as the interface member.

Interfaces are always implemented by more than one class

### Interface may include:

- Constants
- Operators
- Static constructor.
- Nested types
- Static fields, methods, properties, indexers, and events
- Member declarations using the explicit interface implementation syntax.
- Explicit access modifiers (the default access is public).


### What problem does the interface solve?
The basic problem an interface is trying to solve is to separate how we use something from how it is implemented.
So that we can write code that can work with a variety of different implementations of some set of responsibilities without having to specifically handle each implementation.

