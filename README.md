# Sum-of-minimum-elements-of-all-subarrays
Given an array A of n integers. The task is to find the sum of minimum of all possible (contiguous) subarray of A.

BruteForce: The Naive approach is to generate all possible (contiguous) subarrays, find their minimum and add them to result. The time complexity will be O(N2).

Optimized Approach: The general intuition for solution to the problem is to find sum(A[i] * f(i)), where f(i) is the number of subarrays in which A[i] is the minimum.

In order to find f[i], we need to find out: 

left[i], the length of strictly larger numbers on the left of A[i], 
right[i], the length of larger numbers on the right of A[i].
We make two arrays left[ ] and right[ ] such that: 
left[i] + 1 equals to the number of subarrays ending with A[i], and A[i] is only single minimum. 
Similarly, right[i] + 1 equals to the number of subarrays starting with A[i], and A[i] is first minimum.
Finally, f(i) = (left[i]) * (right[i]), where f[i] equals total number of subarrays in which A[i] is minimum.
