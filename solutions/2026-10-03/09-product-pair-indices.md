# Product Pair Indices

**Difficulty:** Easy  
**Topic:** Hash Table

Given an integer array and a target product, return indices of two numbers whose product equals the target.

## Approach
Store each number and its index in a hash map; for each element, check if target divided by it exists in the map.

## Complexity
O(n) time, O(n) space

## Solution
```python
def find_pair(nums,target):\n    seen={}\n    for i,n in enumerate(nums):\n        if n!=0 and target%n==0:\n            comp=target//n\n            if comp in seen:\n                return [seen[comp],i]\n        seen[n]=i\n    return []
```
