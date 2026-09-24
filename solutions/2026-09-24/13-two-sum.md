# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target value, find the indices of two numbers that add up to the target. Return the indices as a list of two integers. Assume exactly one solution exists and you cannot use the same element twice.

## Approach
Use a hash map to store numbers and their indices while iterating. For each number, check if target minus it exists in the map.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []
```
