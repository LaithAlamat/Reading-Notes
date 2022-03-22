## Introduction to Classes
A type that is defined as a class is a reference type. At run time, when you declare a variable of a reference type, the variable contains the value null until you explicitly create an instance of the class by using the new operator, or assign it an object of a compatible type that may have been created elsewhere.

## Declaring Classes
Classes are declared by using the class keyword followed by a unique identifier,The class keyword is preceded by the access level.

## Creating Objects
 A class defines a type of object, but it is not an object itself. An object is a concrete entity based on a class, and is sometimes referred to as an instance of a class.

 Objects can be created by using the new keyword followed by the name of the class that the object will be based on.

 ## Class Inheritance
 Inheritance is accomplished by using a derivation, which means a class is declared by using a base class from which it inherits data and behavior. A base class is specified by appending a colon and the name of the base class following the derived class name.

## Constructors
A constructor is a method whose name is the same as the name of its type. Its method signature includes only an optional access modifier, the method name and its parameter list; it does not include a return type.

## Properties 
A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. Properties can be used as if they are public data members, but they are actually special methods called accessors. This enables data to be accessed easily and still helps promote the safety and flexibility of methods.
- A get property accessor is used to return the property value, and a set property accessor is used to assign a new value. In C# 9 and later, an init property accessor is used to assign a new value only during object construction. These accessors can have different access levels. For more information, see Restricting Accessor Accessibility.

- The value keyword is used to define the value being assigned by the set or init accessor.

## Stack vs. Heap
The Stack is more or less responsible for keeping track of what's executing in our code (or what's been "called").  The Heap is more or less responsible for keeping track of our objects (our data)

The Heap has to worry about Garbage collection (GC) - which deals with how to keep the Heap clean.

- A Reference Type always goes on the Heap.
- Value Types and Pointers always go where they were declared.