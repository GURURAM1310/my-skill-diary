# Remove Duplicates Sorted Array

* **Platform:** GeeksforGeeks
* **Difficulty:** Easy
* **Topic:** Array / Set / Sorting
* **Status:** Solved

## Approach

I used a `set()` to remove duplicate elements from the sorted array.

Then I converted the set back into a list and used `sorted()` to ensure the elements remain in ascending order.

1. Convert the array into a set to remove duplicates.
2. Convert the set back into a list.
3. Sort the resulting list.
4. Return the distinct elements.

## My Solution

```python
class Solution:
    def removeDuplicates(self, arr):
        # code here
        return sorted(list(set(arr)))
```

## Complexity

* **Time Complexity:** `O(n log n)` — due to sorting.
* **Space Complexity:** `O(n)` — for storing the unique elements.

**Key Pattern:** Removing Duplicates Using a Set
