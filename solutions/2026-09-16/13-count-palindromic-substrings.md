# Count Palindromic Substrings

**Difficulty:** Medium  
**Topic:** Strings

Given a string s, count all substrings that are palindromes. Return the count.

## Approach
Expand around each center to count palindromes.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromes(s):
    count=0
    for i in range(len(s)):
        l=r=i
        while l>=0 and r<len(s) and s[l]==s[r]:
            count+=1
            l-=1
            r+=1
        l=i
        r=i+1
        while l>=0 and r<len(s) and s[l]==s[r]:
            count+=1
            l-=1
            r+=1
    return count
```
