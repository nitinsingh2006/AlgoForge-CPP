# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Given the head of a singly linked list, reverse the list and return the new head. The list may be empty.

## Approach
Iteratively rewire pointers using three references: prev, curr, next.

## Complexity
O(n) time, O(1) space

## Solution
```python
class ListNode:\n    def __init__(self,val=0,next=None):\n        self.val=val\n        self.next=next\n\ndef solve(head):\n    prev=None\n    curr=head\n    while curr:\n        nxt=curr.next\n        curr.next=prev\n        prev=curr\n        curr=nxt\n    return prev
```
