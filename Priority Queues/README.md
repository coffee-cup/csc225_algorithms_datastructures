# Priority Queues

### Definition

A **Priority Queue** data structure stores a collection of elements, each with an associated property (also called a 'key'). Priority Queues have two core operations:

1. Insert(e): Add the element *e* to the collection
2. RemoveMin(): Remove (and return) the element in the collection with the lowest priority

![](http://i.imgur.com/P3zK0bT.png)

Applications:

- Job scheduling
- Graph Algorithms

### Sorting with a Priority Queue

Any priority queue *Q* can be used to sort an array *A* of size *n* with a simple algorithm:

- Add each element *A[i]* *Q* with priority *A[i]*
- Call RemoveMin *n* times and store the resulting sequence back to *A*.
When a heap is used to implement the priority queue, the resulting algorithm is Heap Sort, which is *O(n*log*n)* .
