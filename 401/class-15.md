# Trees

**there are some common properties among all trees :**

- Node - A Tree node is a component which may contain it’s own values, and references to other nodes
- Root - The root is the node at the beginning of the tree
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node on the right, in a binary tree
- Right - A reference to the other child node on the left, in a binary tree
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not have any children
- Height - The height of a tree is the number of edges from the root to the furthest leaf

### Traversals
traversing a tree is important it allows us to do many things and make it easy to deal with nodes , there are two way to traverse a tree:  


- Depth First  
 is where we prioritize going through the depth (height) of the tree first, there are three methods for depth first traversal :  
 • Pre-order  
   through recursion every time we start with root and output its value, add it to the call stack, then check if the root has a left it will output its value and be the next root and add it to the stack, it will continue until it reach a leaf node , then it will pop of the stack and the root will be its parent now since it looked for the left node already it will look for the right node , if the right node is a leaf it will pass the root back to its parent and if the parent has already looked to the left and right it will pass it to its parent and so on.  
   the order is : root >> left >> right  

  • In-order: the same as the pre-order but the the order is : left >> root >> right 


  • Post-order: and the order here is left >> right >> root  


- Breadth First  
Breadth first traversal iterates through the tree by going through each level of the tree node-by-node, breadth first traversal uses a queue to traverse the width/breadth of the tree.  
the process in the breadth first, we start with the root and enqueue it , then we dequeue the node that was in the front of the queue and enqueue its children left then right and so on every time you dequeue you enqueue its childs, like this we will traverse the tree level by level. 

### Binary Tree Vs K-ary Trees  

Binary tree: the number is resticted to two in each node which are the left and right  

K-ary Trees: trees that it nodes have more than two childeren in it, in this type of the K is to refer to the maximum number of children that each Node is able to have.  

Breadth First Traversal for the k-ary trees:  
enqueue root -> dequeue root -> enqueue root children and so on until it reach the leaf nodes it will dequeue them (level by level).  

### Adding a node  

there are no structural rules for where nodes are “supposed to go” in a binary tree, it really doesn’t matter where a new node gets placed.  
One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down, we use the breadth first traversal, the first node that doesn't have its childs filled we will insert the new node to be its child.  

**Big O**:  
time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n)  
space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree.

### Binary Search Trees (BST)

in BST the nodes are organized in a way that all values that are smaller than the root are on the left, and all values that are larger than the root are on the right.  

**Searching a BST**  
compare the node you are searching for against the root of the tree or sub-tree. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.  
The `Big O` time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height).  
The Big O space complexity of a BST search would be O(1)  
