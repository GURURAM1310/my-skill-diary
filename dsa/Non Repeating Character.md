# Non Repeating Character

* **Platform:** GeeksforGeeks
* **Difficulty:** Easy
* **Topic:** String / Hashing / Frequency Counting
* **Status:** Solved

## Approach

I used Python's `Counter` to count the frequency of each character in the string.

Then I traversed the string from left to right and checked the frequency of each character. The first character with a frequency of `1` is the first non-repeating character.

If no non-repeating character exists, I return `'$'` as required.

1. Count the frequency of each character using `Counter`.
2. Traverse the string from left to right.
3. Check whether the current character occurs exactly once.
4. Return the first non-repeating character.
5. If no such character exists, return `'$'`.

## My Solution

```python
from collections import Counter

class Solution:
    def nonRepeatingChar(self, s):
        a = Counter(s)
        res = ''

        for i in s:
            if a[i] == 1:
                res += i
                break

        if res == '':
            return -1
        else:
            return res[0]
```

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(k)`, where `k` is the number of distinct characters.
* Since the string contains only lowercase English letters, `k ≤ 26`, so the space complexity is effectively **O(1)**.

**Key Pattern:** Frequency Counting / Hash Map
