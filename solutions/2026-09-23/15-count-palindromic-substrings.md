# Count Palindromic Substrings

**Difficulty:** Medium  
**Topic:** Strings

Count the number of palindromic substrings in a given string. A substring is palindromic if it reads the same forward and backward. Return the total count.

## Approach
Expand around each possible center (including between characters) to count palindromes. This runs in O(n^2) time and O(1) space.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromes(s):\n    n=len(s)\n    res=0\n    for center in range(2*n-1):\n        l=center//2\n        r=l+center%2\n        while l>=0 and r<n and s[l]==s[r]:\n            res+=1\n            l-=1\n            r+=1\n    return res
```
