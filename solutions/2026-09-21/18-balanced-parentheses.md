# Balanced Parentheses

**Difficulty:** Medium  
**Topic:** Strings

Check if a string of parentheses is balanced.

## Approach
Use a stack to match opening and closing brackets.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(s):\n    stack=[]\n    pairs={')':'(',']':'[','}':'{'}\n    for c in s:\n        if c in '([{':\n            stack.append(c)\n        else:\n            if not stack or stack[-1]!=pairs[c]:\n                return False\n            stack.pop()\n    return not stack
```
