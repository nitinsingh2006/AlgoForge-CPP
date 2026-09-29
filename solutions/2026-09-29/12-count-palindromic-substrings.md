# Count Palindromic Substrings

**Difficulty:** Medium  
**Topic:** Strings, DP

Count all palindromic substrings in a given string. A substring is palindromic if it reads the same forwards and backwards.

## Approach
Expand around each center (including between characters) to count palindromes. This runs in O(n^2) time.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromic_substrings(s):
    n=len(s)
    count=0
    for center in range(2*n-1):
        l=center//2
        r=l+center%2
        while l>=0 and r<n and s[l]==s[r]:
            count+=1
            l-=1
            r+=1
    return count
```
