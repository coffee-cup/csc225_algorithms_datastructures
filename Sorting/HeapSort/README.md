# Heap Sort

**Best**: O(nlogn) **Expected**: O(nlogn) **Worse**: O(nlogn)

Heap Sort can be implemented as an in-place algorithm using array-based heaps, by converting the input array to a max-heap using Heapify.

![hs1](http://i.imgur.com/ZvU1J1y.png)

![hs2](http://i.imgur.com/bwfsPdH.png)

Bolded values correspond to elements of valid heaps

![hs3](http://i.imgur.com/ByV55dp.png)

![hs4](http://i.imgur.com/8kuzafh.png)

After the input array has been converted to a max-heap, the RemoveMax operation is used to repeatedly remove the maximum element

![hs5](http://i.imgur.com/GrZNnUn.png)

As each element is removed, it is places at the end of the array, in the position freed up by the remove operation

![hs6](http://i.imgur.com/a957Oik.png)

After the last heap removal, the array is sorted
