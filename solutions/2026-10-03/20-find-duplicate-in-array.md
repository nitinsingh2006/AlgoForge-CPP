# Find Duplicate in Array

**Difficulty:** Easy  
**Topic:** Hashing

Given an array of n+1 integers where each integer is between 1 and n inclusive, find the duplicate number.

## Approach
Use a set to track seen numbers and return the first repeat.

## Complexity
O(n) time, O(n) space

## Solution
```python
def find_duplicate(nums):
    seen = set()
    for num in nums:
        if num in seen:
            return num
        seen.add(num)
    return -1
```
