# Bucket Sort

Simple algorithm for sorting sequences with a small number of possible values.

- A bucket is created for each type of element.
- The first part of bucket sort loops over the input array, adding each element to its respective bucket.

![bs1](http://i.imgur.com/KvWA5O8.png)

To generate sorted array, the buckets are visited in ascending order and each bucket's contents are appened to the array.

![bs2](http://i.imgur.com/Q8DCt7X.png)

Bucket sort is very efficient when sorting on a key with a limited number of values. If there are b bucketsm the running time of bucket sort on an array of size n is O(n+b)
