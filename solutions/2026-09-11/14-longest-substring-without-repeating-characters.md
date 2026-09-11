# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Return the length of the longest substring without duplicate characters.

## Approach
Sliding window with a set to track characters.

## Complexity
O(n) time, O(min(n,alphabet)) space

## Solution
```python
def longest_substring(s):
    seen={}
    left=0
    maxlen=0
    for right,ch in enumerate(s):
        if ch in seen and seen[ch]>=left:
            left=seen[ch]+1
        seen[ch]=right
        maxlen=max(maxlen,right-left+1)
    return maxlen
```
