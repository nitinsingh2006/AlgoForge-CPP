# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked Lists

Given the head of a singly linked list, reverse the list and return the new head. The list may contain any number of nodes.

## Approach
Iteratively traverse the list, reassigning each node's next pointer to the previous node. Maintain three pointers: prev, curr, next. After traversal, prev points to the new head.

## Complexity
O(n) time, O(1) space

## Solution
```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def solve(head):
    prev = None
    curr = head
    while curr:
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt
    return prev
```
