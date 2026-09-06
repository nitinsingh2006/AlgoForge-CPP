# Palindrome Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Check if a singly linked list is a palindrome without extra space.

## Approach
Find middle, reverse second half, compare halves, then restore list.

## Complexity
O(n) time, O(1) space

## Solution
```python
def is_palindrome(head):\n    # Find middle\n    slow, fast = head, head\n    while fast and fast.next:\n        slow, fast = slow.next, fast.next.next\n    # Reverse second half\n    prev = None\n    curr = slow\n    while curr:\n        nxt = curr.next\n        curr.next = prev\n        prev = curr\n        curr = nxt\n    # Compare\n    left, right = head, prev\n    while right:\n        if left.val != right.val:\n            return False\n        left, right = left.next, right.next\n    return True
```
