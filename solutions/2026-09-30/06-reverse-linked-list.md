# Reverse Linked List

**Difficulty:** Easy  
**Topic:** Linked List

Reverse a singly linked list and return the new head.

## Approach
Iterative pointer reversal.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_list(head):
    prev = None
    curr = head
    while curr:
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt
    return prev
```
