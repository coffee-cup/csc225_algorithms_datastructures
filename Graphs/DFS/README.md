# Depth-First Search (DFS)

- Starts at a vertex u and visits every vertex reachable from u
- At each step, a neighbour of the current vertex is chosen to be the next vertex visited
- Edges in the DFS tree may be called **tree edges** or **discovery edges**

![1](http://i.imgur.com/axu3YNo.png)

![2](http://i.imgur.com/6Fd3nA0.png)

![3](http://i.imgur.com/avrsV6j.png)

- The green edge in the diagram cannot be followed by DFS, since it is connected to a previously visited vertex
- Such edges are called **back edges**

![4](http://i.imgur.com/fjVy17D.png)

- At this point, the current vertex has no unvisited neighbours
- Recursion unwinds to the last vertex with unvisited neighbours and the traversal continues from there

![5](http://i.imgur.com/ERHCGHG.png)
