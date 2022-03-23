## Analysis of Algorithm Efficiency

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

- Running Time (also known as time efficiency / complexity)
The amount of time a function needs to complete.

- Memory Space (also known as space efficiency / complexity)
The amount of memory resources a function uses to store data and instructions.

In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:

- Input Size
- Units of Measurement
- Orders of Growth
- Best Case, Worst Case, and Average Case

------------------------------------------------------------------------------------

In order to quantify the Running Time in our analysis, we will consider Three Measurements of time:
The time in milliseconds from the start of a function execution until it ends.
For the purposes of Big O, we won’t be considering this measurement since different machines will have different individual run times depending on how powerful they are. Regardless, this will always be a measurement of run-time.

The number of operations that are executed.
Think of this as the number of lines of code that are executed from start to finish of a function.

The number of “Basic Operations” that are executed.
“Basic Operation” refers to the operation that is contributing the most to the total running time. This is usually the most time consuming operation within the inner most loop.

In order to quantify Memory Space, we can consider Four Sources of Memory Usage during function run-time:
The amount of space needed to hold the code for the algorithm.
Think of this as the number of bytes required to store the characters for the instructions specified in your function.

The amount of space needed to hold the input data.
If direct input data is not considered, we may just refer to this as Additional Memory Space since not all functions have direct input values.

The amount of space needed for the output data.
The amount of space needed to hold working space during the calculation.
Working Space can be thought of as the creation of variables and reference points as our function performs calculations. This will also include Stack Space of recursive function calls … specifically how memory usage scales relatively with the size of the input.

## Linked Lists
A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link. There are two types of Linked List - Singly and Doubly.

When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The best way to approach a traversal is through the use of a while() loop.

One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.

A linked list is made up of a series of nodes, which are the elements of the list.

Head: The starting point of the list is a reference to the first node.

A node has just two parts: data, or the information that the node contains, and a reference to the next node.


## Memory Management
The biggest differentiator between arrays and linked lists is the way that they use memory in our machines.

 Linked lists don’t need to take up a single block of memory; instead, the memory that they use can be scattered throughout.

 - Arrays are static data structures, while linked lists are dynamic data structures. A static data structure needs all of its resources to be allocated when the structure is created; this means that even if the structure was to grow or shrink in size and elements were to be added or removed, it still always needs a given size and amount of memory.
 - Dynamic data structure can shrink and grow in memory. It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.

