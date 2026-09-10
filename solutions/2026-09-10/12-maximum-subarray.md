# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray with the maximum sum.

## Approach
Kadane's algorithm keeps a running sum and max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_so_far=nums[0]\n    cur=nums[0]\n    for n in nums[1:]:\n        cur=max(n,cur+n)\n        max_so_far=max(max_so_far,cur)\n    return max_so_far
```
