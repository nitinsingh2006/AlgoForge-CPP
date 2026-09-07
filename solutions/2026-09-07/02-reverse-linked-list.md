# Reverse Linked List

**Difficulty:** Easy  
**Topic:** Linked Lists

Reverse a singly linked list and return the new head.

## Approach
Iteratively reverse pointers using three variables.

## Complexity
O(n) time, O(1) space

## Solution
```python
class ListNode:\n    def __init__(self,val=0,next=None):\n        self.val=val\n        self.next=next\n\ndef reverse_list(head):\n    prev=None\n    curr=head\n    while curr:\n        nxt=curr.next\n        curr.next=prev\n        prev=curr\n        curr=nxt\n    return prev
```
