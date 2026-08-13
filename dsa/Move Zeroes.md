# 283. Move Zeroes

* **Platform:** LeetCode
* **Difficulty:** Easy
* **Topic:** Array / List Comprehension / In-Place Modification
* **Status:** Solved

## Approach

I used list comprehensions to separate the non-zero and zero elements while preserving their relative order.

The two resulting lists are then combined and assigned back to `nums` using `nums[:]`, which modifies the original list **in-place**.

1. Collect all non-zero elements.
2. Collect all zero elements.
3. Combine both lists, placing zeroes at the end.
4. Use `nums[:]` to update the original array.

## My Solution

```python
class Solution:
    def moveZeroes(self, nums: List[int]) -> None:
        nums[:] = [x for x in nums if x != 0] + [x for x in nums if x == 0]
```

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(n)`

> **Note:** Although `nums[:]` modifies the array in-place, the list comprehensions create new lists, so the solution uses `O(n)` auxiliary space.
