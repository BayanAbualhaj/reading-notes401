# Reading Notes

## Trees:

 Collection of nodes (starting at a root node), where each node is a data structure consisting of a value, together with a list of references to nodes (the “children”), with the constraints that no reference is duplicated, and none points to the root.

 
![](https://open4tech.com/wp-content/uploads/2018/12/tree-data-struct.png)

1. Binary Trees
2. Binary Search Trees
3. K-ary Trees

## Common Terminology

1. Node - A Tree node is a component which may contain it’s own values, and references to other nodes
2. Root - The root is the node at the beginning of the tree
3. K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
4. Left - A reference to one child node, in a binary tree
5. Right - A reference to the other child node, in a binary tree
6. Edge - The edge in a tree is the link between a parent and child node
7. Leaf - A leaf is a node that does not have any children
8. Height - The height of a tree is the number of edges from the root to the furthest leaf

![trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

## Traversals
There are two categories of traversals when it comes to trees:

* Depth First:
    -  Here are three methods for depth first traversal:
        * Pre-order: root » left » right
        * In-order: left » root » right
        * Post-order: left » right » root

* Breadth First
    - Breadth first traversal iterates through the tree by going through each level of the tree node-by-node.

## Binary Tree Vs K-ary Trees
A binary tree restricts the number of children of each node to two. A more general K-ary tree restricts the number of children to K. An K-ary tree is a tree where each node has at most K children where each of the children are non- overlapping K-ary trees.

## K-ary Trees
* If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree.
* In this type of tree we use **K** to refer to the maximum number of children that each Node is able to have.


![k](https://www.cdn.geeksforgeeks.org/wp-content/uploads/maryintial.png)

## Binary Search Trees

A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.


## Binary Trees
Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

![b](https://s3.studylib.net/store/data/009567192_1-d038e09169581a1f430135d4a3101beb.png)