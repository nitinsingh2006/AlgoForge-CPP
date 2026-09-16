# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):best=curr=nums[0];for x in nums[1:]:curr=max(x,curr+x);best=max(best,curr);return best
```
