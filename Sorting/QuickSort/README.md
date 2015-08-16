# Quick Sort

**Best**: O(n) **Expected**: O(nlogn) **Worse**: O(n^2)

Quicksort is a divide and conquer algorithm with three phases

## Split

Choose some **pivot** value p and split the elements of the input array A into a subarray L containing elements less than p and subarray G containing elements greater than p.

## Recurse

Sort the two subarrays L and G

## Merge

Concatenate the sorted L with the element p and the sorted G


![qs1](http://i.imgur.com/ix4U2Cy.png)

At each step, the array is partitioned around a pivot value p into sequences L (elements less than p), E (elements equal to p) and G (elements greater than p)

![qs2](http://i.imgur.com/WbtkwvZ.png)
