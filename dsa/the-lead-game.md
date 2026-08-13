# The Lead Game

- **Platform:** CodeChef
- **Difficulty:** Easy
- **Topic:** Cumulative Sum / Running Difference
- **Status:** Solved

## Problem

Given the scores of two players over multiple rounds, determine the player who achieved the maximum lead at the end of any round and the value of that maximum lead.

## My Approach

I maintained the cumulative score of both players while processing each round.

For every round:

1. Add the current scores to the cumulative scores.
2. Calculate the absolute difference between the cumulative scores.
3. Store the lead.
4. Track which player was leading in that round.
5. After processing all rounds, find the maximum lead and determine the player who achieved it.

## My Solution

```python
n = int(input())

a = 0
b = 0
l = []
p1 = []
p2 = []

for i in range(n):
    c, d = map(int, input().split())

    a += c
    b += d

    l.append(abs(a - b))

    if a > b:
        p1.append(i)
    else:
        p2.append(i)

if l.index(max(l)) in p1:
    print(1, max(l))
else:
    print(2, max(l))
