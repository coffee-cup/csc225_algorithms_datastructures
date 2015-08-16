# Graphs

- a **graph** is a collection of **vertices** and **edges**
- Two vertices which are joined by an edge are said to be **neighbours** or **adjacent**
- The **degree** of a vertex, denoted by deg(v), is the number of edges incident to v
- For two vertices u and w, a **path** between u and w is a sequence of vertices which connects u to w

![path](http://i.imgur.com/Z3bFsTr.png)

- a **cycle** is a path of length at least 1 which begins and ends at the same vertex

![cycle](http://i.imgur.com/ABbkmGI.png)

- a graph G is **connected** if, for every pair of vertices u and w, there exists at least one uw-path

- in an **undirected** graph, edges join pairs of vertices but have no directionality

![undirected](http://i.imgur.com/sXFw26w.png)

- a **directed** graph is a graph in which edges have a direction

![directed](http://i.imgur.com/QZoQqtl.png)

- a **complete** graph is a graph G of n vertices with an edge between every pair of vertices

![complete](http://i.imgur.com/OJaSR8J.png)

- a **tree** is a connected, acyclic graph

![tree](http://i.imgur.com/YERPDC3.png)

## Bipartite

A graph is **bipartite** if the vertices of G can be partitioned into sets X and Y such that no edge connects two vertices in X or two vertices in Y

![bipartite](http://i.imgur.com/23A8Ej7.png)

![bp2](http://i.imgur.com/CabC3Sd.png)

A bipartite graph is also called **2-colourable**, since its vertices can be coloured with two colours such that no edge connects two vertices of the same colour.

A **complete bipartite graph**, denoted K_m,n, consists of a set X of m vertices and set Y of n vertices, will all possible edges between the two sets

![complete bp](http://i.imgur.com/N7YdIV2.png)

## Graph Representation

![graph representation](http://i.imgur.com/xXzD8T3.png)

## Running Time of Traversals

In both DFS and BFS, each vertex is visited and processed at most once.
When a vertex v is visited, the traversal algorithms iterate over all neghbours of v and traverse any unvisited neighbours. The total running time is then

![](http://i.imgur.com/kxXoyIm.png)

Therefore, the running time of DFS and BFS is

![](http://i.imgur.com/I439pFK.png)

## Transitive Closure

The **transitive closure** of a graph G is a graph C containing the vertices of G and an edge uv if v is reachable from u in G.

![tc1](http://i.imgur.com/8Vm0Wgw.png)

- Transitive closures of undirected graphs convert each component into a complete graph
- Computed in O(n^2) time by traversing each component and adding all possible edges between the vertices in the component
