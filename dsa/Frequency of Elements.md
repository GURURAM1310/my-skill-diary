# Frequency of Elements

* **Platform:** GeeksforGeeks
* **Difficulty:** Easy
* **Topic:** Array / Hashing / Frequency Counting
* **Status:** Solved

## Approach

I used Python's `Counter` to count the frequency of each distinct element in the array.

Then I iterated through the frequency map and stored each element along with its frequency as a pair.

1. Use `Counter(arr)` to count the occurrences of each element.
2. Create an empty list to store the results.
3. Iterate through each element and its frequency.
4. Append `[element, frequency]` to the result.
5. Return the resulting list.

## My Solution

```python
from collections import Counter

class Solution:
    def countFreq(self, arr):
        # code here
        a = Counter(arr)
        b = []

        for e, c in a.items():
            b.append([e, c])

        return b
```

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(n)`

**Key Pattern:** Frequency Counting / Hash Map
