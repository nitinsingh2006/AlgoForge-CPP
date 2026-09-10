# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers and a target sum, return indices of two numbers that add up to target. Each input has exactly one solution, and you cannot reuse an element.

## Approach
Use a hash map to store numbers and their indices while iterating. For each number, check if target minus it exists in the map; if so, return the pair.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(nums,target):d={};[d.setdefault(n,i) or d.setdefault(target-n,i) for i,n in enumerate(nums)];return [d[target-n],i] if target-n in d else []
```
