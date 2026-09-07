# Longest Increasing Subsequence Length

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an array of integers, compute the length of the longest strictly increasing subsequence.

## Approach
Maintain a list of smallest tail for each length using binary search; iterate through array updating tails.

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
