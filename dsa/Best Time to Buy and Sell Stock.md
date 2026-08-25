# Best Time to Buy and Sell Stock

* **Platform:** LeetCode
* **Difficulty:** Easy
* **Topic:** Array / Greedy / One Pass
* **Status:** Solved

## Approach

I maintained the **minimum price seen so far** and the **maximum profit** throughout the traversal.

For each price:

1. Update `mi` if the current price is lower than the minimum price seen so far.
2. Otherwise, calculate the profit by selling at the current price.
3. Update `ma` if the current profit is greater than the maximum profit found.
4. Return the maximum profit.

This ensures that the stock is always bought before it is sold.

## My Solution

```python
l = list(map(int, input().split()))

mi = float('inf')
ma = 0

for i in range(len(l)):
    if l[i] < mi:
        mi = l[i]
    elif l[i] - mi > ma:
        ma = l[i] - mi

print(ma)
```

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(n)` — due to storing the input array.

**Key Pattern:** Greedy / Minimum So Far / Single Pass
