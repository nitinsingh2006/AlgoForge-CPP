# Longest Increasing Subsequence Length

**Difficulty:** Hard  
**Topic:** Dynamic Programming

Given an array of integers, find the length of the longest strictly increasing subsequence.

## Approach
Apply patience sorting with binary search to build tails array.

## Complexity
O(n log n) time, O(n) space

## Solution
```python
def length_of_lis(nums):
    import bisect
    tails=[]
    for num in nums:
        i=bisect.bisect_left(tails,num)
        if i==len(tails):
            tails.append(num)
        else:
            tails[i]=num
    return len(tails)
```
