# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array. Return that sum.

## Approach
Kadane’s algorithm keeps current and best sums while scanning.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):\n    best=cur=nums[0]\n    for n in nums[1:]:\n        cur=max(n, cur+n)\n        best=max(best, cur)\n    return best
```
