## Stack
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

### Common terminology for a stack:

- Push - Nodes or items that are put into the stack are pushed
- Pop - Nodes or items that are removed from the stack
- Top - This is the top of the stack.
- Peek - When you peek you will view the value of the top Node in the stack.
- IsEmpty - returns true when stack is empty otherwise returns false.

### Stacks concepts:
 - FILO
First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.

- LIFO
Last In First Out 

This means that the last item added to the stack will be the first item popped out of the stack.


### Push O(1)
Pushing a Node onto a stack will always be an O(1) operation

### Pop O(1)
Popping a Node off a stack is the action of removing a Node from the top.

### Peek O(1)
When conducting a peek, you will only be inspecting the top Node of the stack.


## Queue

### Common terminology for a queue is

- Enqueue - Nodes or items that are added to the queue.
- Dequeue - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
- Front - This is the front/first Node of the queue.
- Rear - This is the rear/last Node of the queue.
- Peek - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
- IsEmpty - returns true when queue is empty otherwise returns false.

### Queues concepts:

- FIFO
First In First Out

This means that the first item in the queue will be the first item out of the queue.

- LILO
Last In Last Out

This means that the last item in the queue will be the last item out of the queue.

### Enqueue O(1)
When you add an item to a queue

### Dequeue O(1)
When you remove an item from a queue

### Peek O(1)
Inspecting the front Node of the queue.

