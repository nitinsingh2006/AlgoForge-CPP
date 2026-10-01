# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps track of current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_ending=max_sofar=nums[0]
    for x in nums[1:]:
        max_ending=max(x,max_ending+x)
        max_sofar=max(max_sofar,max_ending)
    return max_sofar
```
