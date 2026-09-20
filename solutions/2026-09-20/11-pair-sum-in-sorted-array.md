# Pair Sum in Sorted Array

**Difficulty:** Easy  
**Topic:** Arrays

Given a sorted array of integers and a target sum, return indices of two numbers that add up to the target. If none exist, return an empty list.

## Approach
Use two pointers moving inward from both ends.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_pair(nums,target):l,r=0,len(nums)-1;while l<r:s=nums[l]+nums[r];if s==target:return[l,r];elif s<target:l+=1;else:r-=1;return[]
```
