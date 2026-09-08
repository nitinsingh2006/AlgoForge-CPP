# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray within an array that has the largest sum and return that sum.

## Approach
Kadane's algorithm: iterate, keep current max ending here and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    best=curr=nums[0]
    for n in nums[1:]:
        curr=max(n, curr+n)
        best=max(best, curr)
    return best
```
