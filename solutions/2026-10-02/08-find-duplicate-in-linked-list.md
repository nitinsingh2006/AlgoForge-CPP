# Find Duplicate in Linked List

**Difficulty:** Medium  
**Topic:** Linked List

In a singly linked list of n+1 nodes with values 1..n, find the duplicate value. Use O(1) extra space.

## Approach
Apply Floyd's cycle detection to find a meeting point, then reset one pointer to head and move both one step at a time to find the entry node.

## Complexity
O(n) time, O(1) space

## Solution
```python
def findDuplicate(head):
    slow = fast = head
    while True:
        slow = slow.next
        fast = fast.next.next
        if slow is fast:
            break
    ptr1 = head
    ptr2 = slow
    while ptr1 is not ptr2:
        ptr1 = ptr1.next
        ptr2 = ptr2.next
    return ptr1.val
```
