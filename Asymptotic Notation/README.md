# Asymptotic Notation

![an](http://i.imgur.com/NqYvWGQ.png)

## Big-O

Let f(n) and g(n) be functions defined for all n >= 0. If there exist constants c > 0, n0 >= 0 such that

    f(n) <= cg(n)

for all n > n0, then we write

    f(n) in O(g(n))

## Big-Omega

Let f(n) and g(n) be functions defined for all n >= 0. If there exist constants c > 0, n0 >= 0 such that

    f(n) >= cg(n)

for all n > n0, then we write

    f(n) in Omega(g(n))

## Big-Theta

Let f(n) and g(n) be functions defined for all n >= 0. Then f(n) in Theta(g(n)) iff

    f(n) in O(g(n))     and
    f(n) in Omega(g(n))

## Facts

![facts](http://i.imgur.com/GBa0tkc.png)
