# Intuition

The intuition behind this code is based on the binary representation of numbers. A power of two in binary has only one bit set to 1, and all other bits are 0. To determine if a number is a power of two, we can take advantage of this property.

# Approach

- First, we check if n is less than or equal to 0. If n is not a positive integer, it cannot be a power of two, so we return false.
- Next, we use a bitwise operation (n & (n - 1)) to check if there is only one bit set to 1 in the binary representation of n. If the result of this operation is 0, it means that there is only one bit set to 1, which indicates that n is a power of two.
- If the condition in step 2 is met, we return true, indicating that n is a power of two. Otherwise, we return false.

This approach is efficient and doesn't involve any loops or recursion.

# Complexity

- Time complexity:

  - The algorithm runs in constant time as it only involves a few bitwise operations, regardless of the input value n.

- Space complexity:
  - The algorithm uses a fixed amount of space to store variables, and it doesn't rely on any data structures that grow with the input.

# Code

```java
class Solution {
    public boolean isPowerOfTwo(int n) {
        if (n <= 0) {
            return false;
        }
        return (n & (n - 1)) == 0;
    }
}
```
