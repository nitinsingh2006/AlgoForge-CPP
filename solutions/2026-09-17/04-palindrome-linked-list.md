# Palindrome Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Given head of singly linked list, determine if list is palindrome.

## Approach
Find middle, reverse second half, compare halves, restore list.

## Complexity
O(n) time, O(1) space

## Solution
```python
def is_palindrome(head):
    if not head or not head.next:
        return True
    slow, fast = head, head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
    prev = None
    curr = slow
    while curr:
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt
    first, second = head, prev
    while second:
        if first.val != second.val:
            return False
        first = first.next
        second = second.next
    return True
```
