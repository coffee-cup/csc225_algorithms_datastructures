# Sorting Algorithms

![sortingalgo](https://i.gyazo.com/b5d0a59724841e3e1e63ed5445815c24.png)

Any comparison-based sorting algorithm requires Omega(nlogn) operations in the worst case

![sortingalgo2](http://i.gyazo.com/0dc4d7d601bfac435fb2e1352c215b91.png)

## Selection Approach

_left_

Sort the array by moving one element at a time into its sorted position

![selection approach](http://i.imgur.com/NsdvK9Z.png)

## Divide and Conquer Approach

_right_

Sort the array by dividing it into parts, sorting the parts, then combining the sorted parts together

![dandq](http://i.imgur.com/pHeKnZS.png)


## Stable Sorting

A sorting algorithm is **stable** if it guarantees that the order of equal elements is preserved

## In-place algorithms

![inplace](http://i.imgur.com/e1Ycreg.png)

- Some sorting algorithms do all of their work 'inside' the input array.
- Selection sort (left) does not allocate any extra arrays
- Merge sort (right) allocates new arrays fo facilitate recursive sorting and merging
