# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array and two indices L and R, reverse the subarray from L to R inclusive. Return the modified array.

## Approach
Use two-pointer technique to swap elements between L and R.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums,L,R):while L<R:nums[L],nums[R]=nums[R],nums[L];L+=1;R-=1;return nums
```
