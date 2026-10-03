# Longest Increasing Subsequence Length

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the length of the longest strictly increasing subsequence.

## Approach
Use patience sorting: maintain a list of smallest tail for each length; binary search to update tails.

## Complexity
O(n log n) time, O(n) space

## Solution
```python
def length_of_lis(nums):\n    import bisect\n    tails=[]\n    for x in nums:\n        i=bisect.bisect_left(tails,x)\n        if i==len(tails):\n            tails.append(x)\n        else:\n            tails[i]=x\n    return len(tails)
```
