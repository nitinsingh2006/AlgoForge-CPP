# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target, return indices of two numbers that add up to target.

## Approach
Use a hash map to store numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums,target):d={};i=0;while i<len(nums):n=nums[i];if target-n in d:return[d[target-n],i];d[n]=i;i+=1;return[]
```
