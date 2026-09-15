# Balanced Parentheses

**Difficulty:** Easy  
**Topic:** Strings

Determine if a string of parentheses is properly balanced.

## Approach
Use a stack to match opening and closing brackets.

## Complexity
O(n) time, O(n) space

## Solution
```python
def is_balanced(s):
    stack = []
    pairs = {')': '(', ']': '[', '}': '{'}
    for ch in s:
        if ch in '([{':
            stack.append(ch)
        elif ch in ')]}':
            if not stack or stack.pop() != pairs[ch]:
                return False
    return not stack
```
