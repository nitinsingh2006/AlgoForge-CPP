# First Missing Positive

**Difficulty:** Medium  
**Topic:** Arrays

Given an unsorted array of integers, return the smallest missing positive integer.

## Approach
Rearrange numbers so that each positive integer x is placed at index x-1 if possible, then scan for the first index that doesn't match.

## Complexity
O(n) time, O(1) space

## Solution
```python
def first_missing_positive(nums):
    n=len(nums)
    for i in range(n):
        while 1<=nums[i]<=n and nums[nums[i]-1]!=nums[i]:
            nums[nums[i]-1],nums[i]=nums[i],nums[nums[i]-1]
    for i,num in enumerate(nums):
        if num!=i+1:
            return i+1
    return n+1
```
