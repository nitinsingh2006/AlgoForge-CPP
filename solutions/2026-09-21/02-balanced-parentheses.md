# Balanced Parentheses

**Difficulty:** Easy  
**Topic:** Strings

Given a string of parentheses, determine if it is properly balanced.

## Approach
Use a stack to match opening and closing brackets.

## Complexity
O(n) time, O(n) space

## Solution
```python
def is_balanced(s):\n    stack=[]\n    for c in s:\n        if c=='(':\n            stack.append(c)\n        elif c==')':\n            if not stack:\n                return False\n            stack.pop()\n    return not stack
```
