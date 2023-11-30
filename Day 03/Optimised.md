# Intuition:

The intuition behind this code is to efficiently compute Fibonacci numbers using a technique called memoization. The Fibonacci sequence is calculated recursively, and results for intermediate values are stored in a map (`memo`) to avoid redundant calculations and improve performance.

# Approach:

1. The base cases are when `n` is 0 or 1, which are handled without memoization. In such cases, the code returns `n` because the Fibonacci numbers for 0 and 1 are 0 and 1, respectively.

2. The code checks if the result for the current input value (`n`) already exists in the `memo` map. If it does, it directly returns the cached result, avoiding the need for further calculations.

3. If the result for `n` is not found in the `memo`, the code calculates it using a recursive call by adding the results for `n - 1` and `n - 2`.

4. After calculating the result, the code stores it in the `memo` map for future use to improve efficiency.

# Complexity:

- Time complexity: O(n) - The time complexity of this code is linear, as it computes each Fibonacci number only once, and the results are stored in the `memo` map for future reference, preventing redundant calculations.
- Space complexity: O(n) - The space complexity is determined by the depth of the call stack, which is O(n) in this case. Additionally, the `memo` map stores results for each value of `n`, resulting in a space complexity of O(n) as well.

# Code:

```java
class Solution {
    private Map<Integer, Integer> memo = new HashMap<>();

    public int fib(int n) {

        if (n <= 1) {
            return n;
        }

        if (memo.containsKey(n)) {
            return memo.get(n);
        }

        int result = fib(n - 1) + fib(n - 2);
        memo.put(n, result);

        return result;
    }
}
```
