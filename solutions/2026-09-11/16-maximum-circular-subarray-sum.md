# Maximum Circular Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Find the maximum sum of a subarray in a circular array.

## Approach
Apply Kadane for normal and wrap‑around sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_circular(nums):
    max_kadane=cur=nums[0]
    min_kadane=cur_min=nums[0]
    total=nums[0]
    for n in nums[1:]:
        cur=max(n,cur+n)
        max_kadane=max(max_kadane,cur)
        cur_min=min(n,cur_min+n)
        min_kadane=min(min_kadane,cur_min)
        total+=n
    return max_kadane if max_kadane>0 and max_kadane!=total else max(max_kadane,total-min_kadane)
```
