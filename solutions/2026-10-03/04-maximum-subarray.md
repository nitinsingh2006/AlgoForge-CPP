# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray within an array of integers that has the largest sum. Return that sum. The array contains at least one number. Use Kadane's algorithm for linear time.

## Approach
Use Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):max_ending=curr=nums[0];for x in nums[1:]:curr=max(x,curr+x);max_ending=max(max_ending,curr);return max_ending
```
