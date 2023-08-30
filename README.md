# binary_trees
a binary tree is a k-ary tree data structure in which each node has at most two children, which are referred to as the left child and the right child. A recursive definition using just set theory notions is that a (non-empty) binary tree is a tuple (L, S, R), where L and R are binary trees or the empty set and S is a singleton set containing the root. Some authors allow the binary tree to be the empty set as well.
From a graph theory perspective, binary (and K-ary) trees as defined here are arborescences.[3] A binary tree may thus be also called a bifurcating arborescence, before the modern computer science terminology prevailed. It is also possible to interpret a binary tree as an undirected, rather than a directed graph, in which case a binary tree is an ordered, rooted tree.
What is the difference between a binary tree and a Binary Search Tree
-A binary tree and a Binary Search Tree (BST) are both data structures used in computer science to organize and store data in a hierarchical manner. However, there is a significant difference between the two structures in terms of their organization and the rules they follow.
Binary Tree:
A binary tree is a hierarchical data structure where each node can have at most two child nodes, referred to as the left child and the right child. The topmost node is called the root node. Nodes in a binary tree can have zero, one, or two children.

There are no specific rules about the values stored in the nodes of a binary tree. Nodes can be organized in any way, and the tree structure itself doesn't impose any constraints on how the values are ordered.

Binary Search Tree (BST):
A Binary Search Tree (BST) is a type of binary tree that follows a specific ordering rule for the values stored in its nodes. In a BST, for each node:

All nodes in the left subtree have values less than the node's value.
All nodes in the right subtree have values greater than the node's value.
This ordering property allows for efficient searching, insertion, and deletion of values in a BST. Due to this property, the operations on a BST have average-case time complexities of O(log n), making it a useful data structure for maintaining sorted data.

What is the possible gain in terms of time complexity compared to linked lists
The gain in terms of time complexity when using a Binary Search Tree (BST) compared to a linked list depends on the specific operation you're performing. Both data structures have their strengths and weaknesses, and the choice between them depends on the nature of the operations you expect to perform frequently.

What are the depth, the height, the size of a binary tree
Depth:
The depth of a node in a binary tree refers to the distance from the root node to that particular node. The root node itself has a depth of 0. As you move down the tree from the root, the depth of nodes increases by one with each level.

Height:
The height of a binary tree is the length of the longest path from the root node to any leaf node in the tree. It represents the longest distance from the root to any leaf, passing through the maximum number of nodes. The height of an empty tree is typically considered to be -1, and the height of a tree with only one node (the root) is 0.

Size:
The size of a binary tree is the total number of nodes in the tree. It counts all the nodes, including both internal nodes and leaf nodes. In other words, the size of a binary tree reflects the total number of elements stored in the tree.

What are the different traversal methods to go through a binary tree
There are three main methods for traversing (visiting all nodes in a specific order) a binary tree: in-order, pre-order, and post-order traversal. Each method follows a different order for visiting the nodes and serves different purposes depending on the task you want to perform with the tree. Additionally, there's a level-order traversal method, which traverses the tree level by level.

In-Order Traversal:

In an in-order traversal, you visit the nodes in the order of left subtree, current node, right subtree.
This traversal is commonly used in Binary Search Trees (BSTs) to retrieve the nodes in sorted order.
In a BST, in-order traversal produces a sorted sequence of elements.
In pseudocode: inOrder(node) { if node is not null: inOrder(node.left); visit(node); inOrder(node.right); }
Pre-Order Traversal:

In a pre-order traversal, you visit the nodes in the order of current node, left subtree, right subtree.
This traversal is useful for copying the structure of a tree, like making a deep copy or serialization.
In pseudocode: preOrder(node) { if node is not null: visit(node); preOrder(node.left); preOrder(node.right); }
Post-Order Traversal:

In a post-order traversal, you visit the nodes in the order of left subtree, right subtree, current node.
This traversal is commonly used for memory deallocation (e.g., freeing dynamically allocated nodes).
In pseudocode: postOrder(node) { if node is not null: postOrder(node.left); postOrder(node.right); visit(node); }

What is a complete, a full, a perfect, a balanced binary tree
Complete Binary Tree:
A binary tree is considered complete if all levels are completely filled, except possibly the last level, which is filled from left to right.
In a complete binary tree, every level, except possibly the last one, has the maximum number of nodes possible.
Complete binary trees are often used in heap data structures, where the tree remains balanced as elements are inserted or removed.
Complete Binary Tree

Full Binary Tree:
A binary tree is considered full (or proper) if every node has either zero or two children.
In other words, there are no nodes with only one child in a full binary tree.
A full binary tree is also known as a "proper binary tree."
Full Binary Tree

Perfect Binary Tree:
A binary tree is considered perfect if all of its levels are completely filled with the maximum possible number of nodes.
A perfect binary tree has 2^(h+1) - 1 nodes, where 'h' is the height of the tree.
Perfect Binary Tree

Balanced Binary Tree:
A binary tree is considered balanced if the height of the left and right subtrees of any node differs by at most one.
A balanced binary tree ensures that no single branch of the tree grows too deep, resulting in efficient operations like search, insertion, and deletion.
