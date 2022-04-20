# Trees

## Common Terminology

- Node - A Tree node is a component which may contain its own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree
- Right - A reference to the other child node, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

## Traversal

Traversing a tree allows us to search for a node, print out the contents of a tree.

### Traversal Categories:

- Depth First
- Breadth First

## Depth First

Where we prioritize going through the depth (height) of the tree first.

### Methods for depth first traversal:

- Pre-order: root >> left >> right
- In-order: left >> root >> right
- Post-order: left >> right >> root

The most common way to traverse through a tree is to use recursion. With these traversals, we rely on the call stack to navigate back up the tree when we have reached the end of a sub-path.

### Pre-Order

the root has to be looked at first, then the left node set, then right node set

## Breafth First

iterates through the tree by going through each level of the tree node-by-node

breadth first traversal uses a queue (instead of the call stack via recursion)

## K-ary Trees

If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree.

it is similar to the Breadth tree approach

## Binary Search Trees

In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.

The best way to approach a BST search is with a while loop
