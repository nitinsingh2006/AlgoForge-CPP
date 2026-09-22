# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array that sum to a target.

## Approach
Use a hash map to store seen numbers.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums,target):d={};i=0;while i<len(nums):n=nums[i];if target-n in d:return[d[target-n],i];d[n]=i;i+=1;return[]
```
