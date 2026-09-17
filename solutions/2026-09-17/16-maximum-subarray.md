# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm: track current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_so_far=curr=nums[0]
    for n in nums[1:]:
        curr=max(n,curr+n)
        max_so_far=max(max_so_far,curr)
    return max_so_far
```
