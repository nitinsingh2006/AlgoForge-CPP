# Count Palindromic Substrings

**Difficulty:** Medium  
**Topic:** Strings,DP

Count the number of palindromic substrings in a given string. A substring is palindromic if it reads the same forwards and backwards. Return the total count.

## Approach
Expand around each center (2n-1 centers). For each center, expand left and right while characters match, increment count. Complexity O(n^2).

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromic_substrings(s):\n    n=len(s)\n    count=0\n    for center in range(2*n-1):\n        left=center//2\n        right=left+center%2\n        while left>=0 and right<n and s[left]==s[right]:\n            count+=1\n            left-=1\n            right+=1\n    return count
```
