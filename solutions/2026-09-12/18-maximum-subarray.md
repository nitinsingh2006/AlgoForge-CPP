# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps current and global max while iterating.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_ending = max_global = nums[0]
    for num in nums[1:]:
        max_ending = max(num, max_ending + num)
        max_global = max(max_global, max_ending)
    return max_global
```
