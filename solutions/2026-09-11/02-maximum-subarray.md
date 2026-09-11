# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm: iterate, keep current max and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_ending = max_so_far = nums[0]
    for n in nums[1:]:
        max_ending = max(n, max_ending + n)
        max_so_far = max(max_so_far, max_ending)
    return max_so_far
```
