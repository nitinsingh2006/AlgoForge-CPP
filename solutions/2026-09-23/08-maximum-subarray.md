# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray with the largest sum.

## Approach
Kadane's algorithm keeps current and global max while iterating.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_so_far=curr=nums[0]
    for n in nums[1:]:
        curr=max(n,curr+n)
        max_so_far=max(max_so_far,curr)
    return max_so_far
```
