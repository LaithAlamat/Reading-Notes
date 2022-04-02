# Collections

Collections provide a more flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key.

If your collection contains elements of only one data type, you can use one of the classes in the System.Collections.Generic namespace. A generic collection enforces type safety so that no other data type can be added to it. When you retrieve an element from a generic collection, you do not have to determine its data type or convert it.


If the contents of a collection are known in advance, you can use a collection initializer to initialize the collection.

The RemoveAt method causes elements after a removed element to have a lower index value.

You can define a collection by implementing the IEnumerable<T> or IEnumerable interface.

## Some of the common collection classes are described in this section:

- System.Collections.Generic classes: A generic collection is useful when every item in the collection has the same data type. A generic collection enforces strong typing by allowing only the desired data type to be added.

- System.Collections.Concurrent classes: The classes in the System.Collections.Concurrent namespace should be used instead of the corresponding types in the System.Collections.Generic and System.Collections namespaces whenever multiple threads are accessing the collection concurrently.

- System.Collections classes: The classes in the System.Collections namespace do not store elements as specifically typed objects, but as objects of type Object.


## Using LINQ to Access a Collection
LINQ (Language-Integrated Query) can be used to access collections. LINQ queries provide filtering, ordering, and grouping capabilities

## Iterators
An iterator is used to perform a custom iteration over a collection. An iterator can be a method or a get accessor. An iterator uses a yield return statement to return each element of the collection one at a time.

You call an iterator by using a foreach statement.

## Enumeration types
An enumeration type (or enum type) is a value type defined by a set of named constants of the underlying integral numeric type. To define an enumeration type, use the enum keyword and specify the names of enum members

the associated constant values of enum members are of type int; they start with zero and increase by one following the definition text order. You can explicitly specify any other integral numeric type as an underlying type of an enumeration type. You can also explicitly specify the associated constant values, 

