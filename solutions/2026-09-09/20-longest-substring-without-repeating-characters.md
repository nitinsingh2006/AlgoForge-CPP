# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find length of longest substring with all unique characters.

## Approach
Sliding window with a set to track characters.

## Complexity
O(n) time, O(min(n, m)) space

## Solution
```python
def solve(s):
    seen={}
    l=0
    ans=0
    for r,ch in enumerate(s):
        if ch in seen and seen[ch]>=l:
            l=seen[ch]+1
        seen[ch]=r
        ans=max(ans, r-l+1)
    return ans
```
