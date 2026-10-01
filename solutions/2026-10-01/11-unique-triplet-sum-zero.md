# Unique Triplet Sum Zero

**Difficulty:** Medium  
**Topic:** Arrays

Given an array of integers, count the number of unique triplets (i, j, k) with i < j < k such that nums[i] + nums[j] + nums[k] == 0.

## Approach
Sort the array. For each index i, use two pointers left=i+1 and right=n-1 to find pairs that sum to -nums[i], skipping duplicates.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_zero_triplets(nums):
    nums.sort()
    n=len(nums)
    count=0
    for i in range(n-2):
        if i>0 and nums[i]==nums[i-1]:
            continue
        left=i+1
        right=n-1
        while left<right:
            s=nums[i]+nums[left]+nums[right]
            if s==0:
                count+=1
                left+=1
                right-=1
                while left<right and nums[left]==nums[left-1]:
                    left+=1
                while left<right and nums[right]==nums[right+1]:
                    right-=1
            elif s<0:
                left+=1
            else:
                right-=1
    return count
```
