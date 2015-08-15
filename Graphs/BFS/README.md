# Breadth First Traversal
![](http://i.imgur.com/6GICOU5.png)
at each iteration, the vertex at the front of the queue is removed and all of its unvisited neighbours are added to the queue.
![](http://i.imgur.com/3yyjj9Z.png)
![](http://i.imgur.com/HDSemo1.png)
![](http://i.imgur.com/zKSamp6.png)
![](http://i.imgur.com/xxuDcaM.png)
![](http://i.imgur.com/Ik9tMet.png)
![](http://i.imgur.com/mGcJIUj.png)
![](http://i.imgur.com/fqmi3kr.png)
Even though v_6 hasn't been visited yet, it has already been added to the BFS tree (and the queue).
![](http://i.imgur.com/QUcE1pB.png)
![](http://i.imgur.com/pzW6xbH.png)
![](http://i.imgur.com/2z83jFi.png)
![](http://i.imgur.com/S6ck25q.png)
![](http://i.imgur.com/dgrEJaS.png)
![](http://i.imgur.com/SjucCD3.png)
![](http://i.imgur.com/61nTvuP.png)
![](http://i.imgur.com/sE7TaxS.png)
![](http://i.imgur.com/Wv4ftdV.png)
![](http://i.imgur.com/2wDN3Fj.png)
![](http://i.imgur.com/tSgsRY4.png)

A BFS is a more 'conservative' traversal and spreads out slowly from the starting vertex.
As a result, BFS trees have several valuable properties that DFS trees lack.
In particular, the path from any node to the root in a BFS tree is guaranteed to be the shortest path possible.
