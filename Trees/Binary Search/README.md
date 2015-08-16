# Binary Search

> BinarySearch is a O(logn) solution to the SortedArraySearch problem.

The binary search algorithm is a method to find an element in a sorted array in O(logn) time.

The algorithm begins by comparing the target value to vale of the middle element of the sorted array. If the target value is equal to the middle element's value, the position is returned. If the target value is smaller, the saerch continues on the lower half of the array, or if the target value is larger, the search continues until the element is found and its position is returned, or there are no more elements left to search for in the array and a "not found" indicator is returned.

![bs1](https://i.imgur.com/yoHv0WP.png)

**Idea**: Represent the set of possible paths of the binary search algorithm with a linked structure.

![bs2](https://i.imgur.com/pc1zhkX.png)

## Inserting

![bs3](https://i.imgur.com/3PnkFXC.png)

Inserting an element into a binary search tree is O(1) after the correct location has been found
