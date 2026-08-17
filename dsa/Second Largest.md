# Second Largest

* **Platform:** GeeksforGeeks
* **Difficulty:** Easy
* **Topic:** Array / Sorting / Set
* **Status:** Solved

## Approach

I first removed duplicate elements using `set()` because the second largest element must be **distinct** from the largest element.

Then I sorted the unique elements in ascending order.

1. Convert the array into a set to remove duplicates.
2. Convert the set back into a list.
3. Sort the list.
4. If fewer than two distinct elements exist, return `-1`.
5. Otherwise, return the second-last element using `a[-2]`.

## My Solution

```python
class Solution:
    def getSecondLargest(self, arr):
        # code here
        a = sorted(list(set(arr)))

        if len(a) < 2:
            return -1

        return a[-2]
```

## Complexity

* **Time Complexity:** `O(n log n)` — due to sorting the unique elements.
* **Space Complexity:** `O(n)` — for storing the unique elements.

**Key Pattern:** Removing Duplicates + Sorting
