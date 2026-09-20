# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Return the largest sum of a contiguous subarray.

## Approach
Kadane's algorithm keeps current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_ending=max_global=nums[0]
    for x in nums[1:]:
        max_ending=max(x,max_ending+x)
        max_global=max(max_global,max_ending)
    return max_global
```
