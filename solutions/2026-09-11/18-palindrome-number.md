# Palindrome Number

**Difficulty:** Easy  
**Topic:** Math

Check if an integer reads the same backward as forward.

## Approach
Convert to string and compare with reverse.

## Complexity
O(d) time, O(d) space

## Solution
```python
def is_palindrome(x):
    s = str(x)
    return s == s[::-1]
```
