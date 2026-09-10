# Count Palindromic Substrings

**Difficulty:** Medium  
**Topic:** Strings

Given a string s, count the number of substrings that are palindromes. Return the count.

## Approach
Expand around each possible center to count palindromic substrings.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def solve(s):
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
