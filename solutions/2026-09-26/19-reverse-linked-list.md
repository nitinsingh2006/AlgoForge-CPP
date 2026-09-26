# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Given the head of a singly linked list, reverse the list and return the new head.

## Approach
Iteratively traverse the list, reassigning next pointers while maintaining previous node reference.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverseList(head):
    prev = None
    curr = head
    while curr:
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt
    return prev
```
