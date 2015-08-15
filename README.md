# csc225_algorithms_datastructures
### Running Time of Traversals
In both DFS and BFS, each vertex is visited and processed at most once.
When a vertex v is visited, the traversal algorithms iterate over all neghbours of v and traverse any unvisited neighbours. The total running time is then $$n + \sum_{v\in V(G)}deg(v) = n + 2m $$
Therefore, the running time of DFS and BFS is $\Theta (n+m)$.
