# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find the length of the longest substring without repeating characters in a given string.

## Approach
Sliding window with a set to track characters.

## Complexity
O(n) time, O(min(n,m)) space

## Solution
```python
def solve(s):\n    seen={}\n    left=0\n    maxlen=0\n    for right,ch in enumerate(s):\n        if ch in seen and seen[ch]>=left:\n            left=seen[ch]+1\n        seen[ch]=right\n        maxlen=max(maxlen,right-left+1)\n    return maxlen
```
