# Palindrome Linked List

**Difficulty:** Hard  
**Topic:** Linked List

Determine if a singly linked list is a palindrome.

## Approach
Find middle, reverse second half, compare.

## Complexity
O(n) time, O(1) space

## Solution
```python
def is_palindrome(head):
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
    prev = None
    while slow:
        nxt = slow.next
        slow.next = prev
        prev = slow
        slow = nxt
    left, right = head, prev
    while right:
        if left.val != right.val:
            return False
        left = left.next
        right = right.next
    return True
```
