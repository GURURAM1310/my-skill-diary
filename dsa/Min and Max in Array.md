# Min and Max in Array

* **Platform:** GeeksforGeeks
* **Difficulty:** Basic
* **Topic:** Array / Min-Max
* **Status:** Solved

## Approach

I used Python's built-in `min()` and `max()` functions to find the minimum and maximum elements in the array.

1. Use `min(arr)` to find the smallest element.
2. Use `max(arr)` to find the largest element.
3. Return both values as a list in the required `[minimum, maximum]` format.

## My Solution

```python
class Solution:
    def getMinMax(self, arr):
        # code here
        return [min(arr), max(arr)]
```

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(1)`

**Key Pattern:** Array Traversal / Built-in Min-Max Functions
