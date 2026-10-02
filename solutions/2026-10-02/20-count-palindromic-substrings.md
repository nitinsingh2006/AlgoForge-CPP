# Count Palindromic Substrings

**Difficulty:** Hard  
**Topic:** Strings

Count all substrings of a string that are palindromes.

## Approach
Expand around each center; odd and even lengths.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromes(s):
    n=len(s)
    cnt=0
    for i in range(n):
        l=r=i
        while l>=0 and r<n and s[l]==s[r]:
            cnt+=1
            l-=1
            r+=1
        l=r=i+1
        while l>=0 and r<n and s[l]==s[r]:
            cnt+=1
            l-=1
            r+=1
    return cnt
```
