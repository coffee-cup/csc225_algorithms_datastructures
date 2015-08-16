# Minimum Weight Spanning Tree

## Edge-Weighted Graphs

An **edge-weighted** graph is a graph in which each edge is associated with a numerical weight value

![edge-weighted graph](http://i.imgur.com/k28PwFc.png)

weights are useful for modelling qualitative properties, such as 'cost' or 'distance', which are not modelled by the graph structure itself.

- A **minimum weight spanning tree** (MWST) is a spanning tree that connects all vertices in the graph, where the spanning tree weight is less than or equal to the weight of every other spanning tree

![mwst](http://i.imgur.com/PxKubJS.png)

## Finding a MWST of G

Let G be a connected. undirected, edge-weighted graph with n vertices and m edges

### Brute-Force Approach

Generate all spanning trees of G and choose the one with the lowest weight

However, G might have an exponential number of spanning trees

### Cycle Property

In any cycle in G, one edge with the largest weight is not in any MWST

The algorithm is O(n^3)

### Cut Property

If the vertices of G are partitioned into sets S and V(G) - S, the lowest-weight edge between the two parts will be in the MWST

An MWST for G can be created by finding the edges in each part which are part of the MWST, then adding the bridging edge with the lowest-weight

### Baruvka's Algorithm

*component-centric*

The algorithm builds a spanning tree by starting with an empty graph and repeatedly adding edges from the original graph G

![ba1](http://i.imgur.com/E3scFSA.png)

For each component C, the lowest weight edge leaving the component is found

![ba2](http://i.imgur.com/fO62lix.png)

After the lowest weight edge is found, it is added to the spanning graph, which causes the two components to merge

![ba3](http://i.imgur.com/9I28KsV.png)

After all of the original components have been processed, the process is repeated, until only one component remains

![ba4](http://i.imgur.com/HW6RI8G.png)

The sets of edges forms a spanning tree, and the total weight is minimum due to the cut property

- The total running time of Baruvka's algorithm is O((n + m) logn)

### Kruskal's Algorithm

*edge-centric*

Like Baruvka's, Kruskal's algorithm also merges smaller trees to produce a spanning tree

![ka1](http://i.imgur.com/jLqmtNW.png)

At each step of Kruskal's algorithm, the smallest weight edge which joins two components is found and added to the spanning tree

![ka2](http://i.imgur.com/0QFLQUV.png)

![ka3](http://i.imgur.com/IQO0pHt.png)

![ka4](http://i.imgur.com/x7FRZQd.png)

Eventually, only one connected component remains, whcih is a MWST

- Can be implemented to achieve a running time of O(mlogn) with a **union-find** data structure

### Prim-Jarnik Algorithm

*vertex-centric*

Expands a tree outwards from a single vertex until it spans the entire graph

![pja1](http://i.imgur.com/Hk2fQAr.png)

Start by choosing an arbitrary root vertex

![pja2](http://i.imgur.com/gyvf7KG.png)

At each step, find the lowest-weight edge which crosses from the tree to the rest of the graph and add it to the tree

![pja3](http://i.imgur.com/ZDd5v9x.png)

Adding an edge to the tree is called 'relaxing' the edge

![pja4](http://i.imgur.com/hM4VXzh.png)

Eventually, every vertex is part of the tree, which is a MWST, and the algorithm terminates

- When implemented with an adjacency list and heap, the Prim-Jarnik algorithm requires O((n+m) logn) time
- Using a special type of heap called a Fibonacci Heap, the Prim-Jarnik algorithm can achieve O(nlogn) time in the worst case
