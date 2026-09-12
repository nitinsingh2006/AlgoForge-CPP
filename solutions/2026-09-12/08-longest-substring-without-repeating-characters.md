# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find the length of the longest substring without duplicate characters in a given string.

## Approach
Sliding window with a set to track current characters.

## Complexity
O(n) time, O(min(n,alphabet)) space

## Solution
```python
def solve(s):
    seen={}
    left=0
    best=0
    for right,ch in enumerate(s):
        if ch in seen and seen[ch]>=left:
            left=seen[ch]+1
        seen[ch]=right
        best=max(best,right-left+1)
    return best
```
