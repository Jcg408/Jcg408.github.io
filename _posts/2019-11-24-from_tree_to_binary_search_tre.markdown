---
layout: post
title:      "From Tree to Binary Search Tree"
date:       2019-11-24 12:28:10 -0500
permalink:  from_tree_to_binary_search_tre
---



**Data Tree**

A tree is a non linear data structure with branches. A tree is a widely used data type that simulates a hierarchical tree structure. All data points in the tree are called `nodes`. The naming of nodes in a data tree are very similar to a family tree.

The top of the tree is the `root` node which branches out to `child`. Children nodes with branches leading to other nodes are called `parents`. A node which has no children are called `leaf` nodes. Nodes which are children of the same parent node are called `siblings`. 

By convention, the tree is illustrated with the root at the top with the tree growing downward.


**Binary Tree** 

A tree whose nodes have at most 2 children is called a binary tree. Since each node in a binary tree can have only 2 children, we typically name them the left and right child. 



A Binary Tree node contains following parts: 
1) Data
2) Pointer to left child
3) Pointer to right child

**Binary Search Tree**

A binary search tree is a type of ordered binary tree. The nodes in a binary search tree must be sorted. The nodes which have lesser value are stored in the left subtree and the nodes with higher value are stored in the right subtree.
![](https://imgur.com/a/z3JMjhO)
Binary search tree uses the principle of binary search. On average, this will use only half of the tree for search, insertion or deletion which reduces the time complexity of searching the entire tree. This is an advantage over a linear search especially for large numbers. Looking at an array of 1,000,000 elements, the binary search is O(log n) with a worst case of only 20 comparisons. A linear search of the same, O(n), on average will take 500,000 comparisons to search for an element. Binary search is faster on average. 

The limitations of binary search are that the tree must be sorted and the tree must be balanced. The left subtree and right subtree must have the same height. This would need to be checked after insertion or deletion operations.



