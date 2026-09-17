# Reverse Linked List

**Difficulty:** Easy  
**Topic:** Linked Lists

Given the head of a singly linked list, reverse the list and return the new head.

## Approach
Iteratively traverse the list, reversing pointers one by one. Maintain prev and curr pointers.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverseList(head): prev=None; curr=head; while curr: nxt=curr.next; curr.next=prev; prev=curr; curr=nxt; return prev
```
