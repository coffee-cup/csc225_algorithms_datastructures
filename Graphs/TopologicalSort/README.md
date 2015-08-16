# Topological Sorting

A **directed acyclic graph** (DAG) is a directed graph with no directed cycles

![dag](http://i.imgur.com/42RGG9h.png)

a **minimum** is a vertex with no incoming edges

![dag mins](http://i.imgur.com/eXDbcRq.png)

a **maximum** is a vertex with no outgoing edges

![dag maxs](http://i.imgur.com/YrHCCl1.png)

A **topologically sorted ordering** of the vertices of a directed acyclic graph G is a listing of vertices such that if (u, v) in E(G), then u appears before v in the listing.

![toposort](http://i.imgur.com/h7gMkWr.png)

*e.g. In the graph above, the ordering c, a, b, e, d is topologically sorted*

![toposort2](http://i.imgur.com/MvkBCd6.png)

A graph may have multiple topologically sorted orderings


## Finding Topologically Sorted Ordering

### Topologically Sort BFS

![tsa1](http://i.imgur.com/PHNGF4N.png)

Start by adding all minimum vertices to the queue

![tsa2](http://i.imgur.com/UHIPrAN.png)

At each step, remove a vertex from the front of the queue and add it to the topologically sorted ordering

![tsa3](http://i.imgur.com/NwaNNSl.png)

As each vertex is processed, delete it and all incident edges from the graph

![tsa4](http://i.imgur.com/ePBd5zG.png)

When a vertex is deleted, inspect all of its neighbours and add any new minimum vertices to the queue

![tsa5](http://i.imgur.com/CIRjPfR.png)

Vertices d and h are added to the queue

![tsa6](http://i.imgur.com/SZ7UyZY.png)

When i is deleted, vertex b becomes a minimum

![tsa7](http://i.imgur.com/a3eBVje.png)

The algorithm is essentially BFS with one extra condition governing when a vertex can be visited

### Topologically Sort BFS

A post-ordering of vertices in a DFS traversal is topologically sorted.
Constructs the ordering in reverse

![dfst1](http://i.imgur.com/yL0C33l.png)

![dfst2](http://i.imgur.com/ggAoZd3.png)

In the diagram above, the vertex being visited is green and other vertices in the same branch of the DFS tree are blue

![dfst3](http://i.imgur.com/YAwshS8.png)

Vertices are added to the **beginning** of the ordering when DFS unwinds from them

![dfst4](http://i.imgur.com/qCYuqrW.png)

After finishing at f, DFS unwinds

![dfst5](http://i.imgur.com/X8JNXvg.png)

DFS may need to be restarted several times before the entire graph is covered

![dfst6](http://i.imgur.com/Ffpbos6.png)

Although several separate traversals were required, each vertex was visited exactly once
