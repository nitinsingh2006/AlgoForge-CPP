# Longest Increasing Subsequence

**Difficulty:** Hard  
**Topic:** Dynamic Programming

Given an array of integers, find the length of the longest strictly increasing subsequence.

## Approach
Apply patience sorting with binary search to maintain tails of subsequences.

## Complexity
O(n log n) time, O(n) space

## Solution
```python
def length_of_lis(nums):
    import bisect
    tails=[]
    for x in nums:
        i=bisect.bisect_left(tails,x)
        if i==len(tails):
            tails.append(x)
        else:
            tails[i]=x
    return len(tails)
```
