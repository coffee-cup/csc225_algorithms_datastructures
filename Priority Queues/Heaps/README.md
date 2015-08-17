# Heaps

A **heap** is a specialized binary tree data structure with two extra properties:

 - **Heap Property**: The value at a node must be less than or equal to the values of its children
 -
 - **Shape Property**: A heap must be a complete binary tree

### Heap Insertion
![1](http://i.imgur.com/pZcdIMF.png)

First, a new node for element 6 is allocated in the next available position on the last level. (This maintains the *shape property*)
![2](http://i.imgur.com/VAeZVCJ.png)

After the element is added, the heap property is restored.
![3](http://i.imgur.com/i92sd3h.png)

![4](http://i.imgur.com/1I8sbaC.png)

### Heap Removal
![1](http://i.imgur.com/nSmGqNy.png)

To remove the minimum, the element at the root is deleted from the tree.
![2](http://i.imgur.com/xB5AGJN.png)

To fill the 'hole' left by the deleted element, the last element in the last row is moved into the empty position
![3](http://i.imgur.com/wyr6kg6.png)

The heap property is restored by 'bubbling down' the new root
![4](http://i.imgur.com/25rblo3.png)

![5](http://i.imgur.com/1VH1B1A.png)

![6](http://i.imgur.com/25THezK.png)

![7](http://i.imgur.com/nKuCVKv.png)

### The Height of a Heap

**Theorem**: In a heap with with height *h*, there are exactly *2^i* nodes at levels *0, 1, 2, ..., h-1* and at most *2^h* nodes at level *h*.

**Proof Outline**:
A heap of height 0 is a single node, and the theorem holds. The theorem can be proven by induction using h = 0 as a basis. The induction step should use a combination of the hypothesis and the shape property.

**Corollary**: In a heap with *n* nodes and height *h*, *h <= log_2(n)*

### Array Based Heaps
Heaps can be represented be an array with a convenient numbering scheme
![Array-Based Heap](http://i.imgur.com/RBptAPQ.png)

 - Nodes are numbered level by level, from left to right, starting at the root.
 - This indexing scheme allows convenient traversal of the tree
    - Parent(i) = i/2 (integer division)
    - LeftChild(i) = 2i
    - RightChild(i) = 2i + 1


 ### Heapify
 ![array](http://i.imgur.com/la4dBr3.png)

 To create a heap containing the values in the array, create an empty heap and add elements one-by-one.

 This requires */theta(n* log *n*) operations, because the last *n/2* insertions will be into a tree of height at least log_2(n-1).

 It is also possible to build a heap with bottom-up approach, using an algorithm called **Heapify**.

 ![4](http://i.imgur.com/ReUxzaY.png)

 A complete binary tree containing the input sequence is created and gradually converted into a heap from the bottom to the top.

 First, all single nodes are converted into heaps

 ![6](http://i.imgur.com/5YTYrbL.png)

 Next, convert the subtrees of height 1 to heaps.

 ![8](http://i.imgur.com/cOiPuML.png)

 The bottom-up construction merges subtrees into larger heaps repeatedly, working upwards from the bottom of the tree.

 ![9](http://i.imgur.com/JS58edm.png)

 Eventually, the entire tree is a heap.

 > **Claim**: *Heapify* constructs a heap of *n* elements with */theta(n)* operations.
 > **Proof**: A cursory analysis seems to suggest that the *n* bubble-down operations require */theta(nlog(n))* operations. To prove that only */theta(n)* operations are necessary, we will consider the operations at each level of the tree separately.
 > ![14](http://i.imgur.com/JS58edm.png)

 > ![15](http://i.imgur.com/aiz3w6z.png)
