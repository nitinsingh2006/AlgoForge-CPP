# Balanced Parentheses

**Difficulty:** Easy  
**Topic:** Strings

Given a string of parentheses '(', ')', '{', '}', '[' and ']', determine if it is properly balanced.

## Approach
Use a stack to match opening and closing.

## Complexity
O(n) time, O(n) space

## Solution
```python
def is_balanced(s):\n    stack=[]\n    mapping={')':'(', '}':'{', ']':'['}\n    for ch in s:\n        if ch in mapping.values():\n            stack.append(ch)\n        elif not stack or stack.pop()!=mapping[ch]:\n            return False\n    return not stack
```
