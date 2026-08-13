# 387. First Unique Character in a String
-**Platform:** LeetCode
-**Difficulty:** Easy
-**Topic:** String / Frequency Counting / Hashing
-**Status:** Solved
## Approach

I used Counter to store the frequency of each character in the string.

Then I traversed the string from left to right:

Count the frequency of every character using Counter.
Check each character's frequency.
If the frequency is 1, return its index.
If no unique character exists, return -1.
## My Solution

python
from collections import Counter

class Solution:
    def firstUniqChar(self, s: str) -> int:
        c = Counter(s)

        for a, b in enumerate(s):
            if c[b] == 1:
                return a

        return -1

-**Complexity**
- **Time Complexity:** O(n)
-**Space Complexity:** O(k), where k is the number of distinct characters.
Since the string contains only lowercase English letters, the space complexity is effectively O(1).
