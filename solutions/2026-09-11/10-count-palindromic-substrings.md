# Count Palindromic Substrings

**Difficulty:** Medium  
**Topic:** Strings

Count all substrings of a string that are palindromes.

## Approach
Expand around each center, counting palindromes as the expansion succeeds.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromes(s):
    n = len(s)
    count = 0
    for center in range(2*n-1):
        left = center//2
        right = left + center%2
        while left>=0 and right<n and s[left]==s[right]:
            count+=1
            left-=1
            right+=1
    return count
```
