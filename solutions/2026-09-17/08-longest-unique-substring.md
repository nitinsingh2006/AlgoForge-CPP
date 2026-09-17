# Longest Unique Substring

**Difficulty:** Easy  
**Topic:** Strings

Find the length of the longest substring without repeating characters.

## Approach
Sliding window with a set.

## Complexity
O(n) time, O(1) space

## Solution
```python
def longest_unique_substring(s):
    seen={}
    left=0
    max_len=0
    for right,ch in enumerate(s):
        if ch in seen and seen[ch]>=left:
            left=seen[ch]+1
        seen[ch]=right
        max_len=max(max_len,right-left+1)
    return max_len
```
