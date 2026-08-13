# 53. Maximum Subarray

* **Platform:** LeetCode
* **Difficulty:** Medium
* **Topic:** Array / Dynamic Programming / Kadane's Algorithm
* **Status:** Solved

## Approach

I used **Kadane's Algorithm** to find the maximum sum of a contiguous subarray in linear time.

I maintained two variables:

* `curr` — the maximum subarray sum ending at the current position.
* `maxi` — the maximum subarray sum found so far.

For each element:

1. Decide whether to start a new subarray from the current element or extend the existing subarray.
2. Update `curr` using `max(c, curr + c)`.
3. Update `maxi` with the maximum value of `curr`.
4. Return `maxi` after traversing the entire array.

## My Solution

```python
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        curr, maxi = 0, -inf

        for c in nums:
            curr = max(c, curr + c)
            maxi = max(maxi, curr)

        return maxi
```

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(1)`

**Key Pattern:** Kadane's Algorithm — a fundamental technique for solving maximum subarray sum problems efficiently.
