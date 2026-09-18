# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array nums and two indices left and right, reverse the subarray nums[left..right] in place and return the modified array.

## Approach
Use two pointers starting at left and right, swap elements until they meet.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums, left, right):
    while left < right:
        nums[left], nums[right] = nums[right], nums[left]
        left += 1
        right -= 1
    return nums
```
