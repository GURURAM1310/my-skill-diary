# Longest Substring with Distinct Characters

* **Platform:** GeeksforGeeks
* **Difficulty:** Medium
* **Topic:** String / Sliding Window / Two Pointers
* **Status:** Solved

## Approach

I used a **sliding window** approach to maintain a substring containing only distinct characters.

I stored the current substring in `a`. When a new character was not already present, I added it to the substring. If the character was already present, I moved the start of the substring to the position after its previous occurrence and continued.

1. Maintain the current substring using `a`.
2. If the current character is not present in `a`, add it.
3. If it is already present, update the maximum length.
4. Remove the characters before and including its previous occurrence.
5. Add the current character and continue.
6. Return the maximum length found.

## My Solution

```python id="4xq8fz"
class Solution:
    def longestUniqueSubstr(self, s):
        # code here
        a = ''
        c = 0
        m = 0

        for i in range(len(s)):
            if s[i] not in a:
                a += s[i]
            else:
                m = max(m, len(a))
                a = a[a.index(s[i]) + 1:] + s[i]

        return max(m, len(a))
```

## Complexity

* **Time Complexity:** `O(n²)` in the worst case because searching within the string and slicing can take `O(n)`.
* **Space Complexity:** `O(n)` for storing the current substring.

**Key Pattern:** Sliding Window / Two Pointers

> **Note:** Your approach is logically correct, but for `n ≤ 10⁵`, an optimized sliding-window solution using a set or dictionary can achieve **O(n)** time.
