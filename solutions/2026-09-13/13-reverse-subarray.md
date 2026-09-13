# Reverse Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Given an array nums and two indices left and right, reverse the subarray nums[left..right] in place and return the modified array.

## Approach
Use two pointers starting at left and right, swapping elements until they meet.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums,left,right):\n    while left<right:\n        nums[left],nums[right]=nums[right],nums[left]\n        left+=1\n        right-=1\n    return nums
```
