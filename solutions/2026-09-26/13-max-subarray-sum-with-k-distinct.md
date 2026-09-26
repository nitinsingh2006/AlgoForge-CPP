# Max Subarray Sum with K Distinct

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array nums and an integer k, find the maximum sum of any contiguous subarray that contains at most k distinct numbers.

## Approach
Use a sliding window with a hash map to track element counts and maintain at most k distinct elements.

## Complexity
O(n) time, O(k) space

## Solution
```python
def max_subarray_k_distinct(nums, k):
    from collections import defaultdict
    left = 0
    count = defaultdict(int)
    distinct = 0
    max_sum = 0
    cur_sum = 0
    for right, val in enumerate(nums):
        if count[val] == 0:
            distinct += 1
        count[val] += 1
        cur_sum += val
        while distinct > k:
            left_val = nums[left]
            count[left_val] -= 1
            cur_sum -= left_val
            if count[left_val] == 0:
                distinct -= 1
            left += 1
        if cur_sum > max_sum:
            max_sum = cur_sum
    return max_sum
```
