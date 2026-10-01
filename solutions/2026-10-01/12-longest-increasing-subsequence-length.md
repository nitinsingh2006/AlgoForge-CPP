# Longest Increasing Subsequence Length

**Difficulty:** Hard  
**Topic:** DP

Given an array of integers, return the length of the longest strictly increasing subsequence.

## Approach
Maintain a list tails. For each number, binary search its position in tails and replace or append to keep tails sorted.

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
