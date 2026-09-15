# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array and two indices left and right, reverse the subarray between them inclusive.

## Approach
Use two‑pointer technique to swap elements until pointers cross.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums,left,right):
    while left<right:
        nums[left],nums[right]=nums[right],nums[left]
        left+=1
        right-=1
    return nums
```
