# Reverse Linked List

**Difficulty:** Easy  
**Topic:** Linked Lists

Reverse a singly linked list and return its new head.

## Approach
Iteratively rewire pointers while traversing.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_list(head):
    prev=None
    curr=head
    while curr:
        nxt=curr.next
        curr.next=prev
        prev=curr
        curr=nxt
    return prev
```
