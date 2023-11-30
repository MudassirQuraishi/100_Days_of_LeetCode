# Intuition

The intuition behind this code is to determine if a given integer n is a power of two. To check this, the code repeatedly divides n by 2 until n becomes 1 or an odd number. If n becomes 1, it is considered a power of 2. If n becomes an odd number, it is not a power of 2. If n is initially 0, it's also considered not a power of 2.

# Approach

- First, check if n is equal to 0. If it is, return false because 0 is not a power of 2.
- Use a while loop to repeatedly divide n by 2 while n is even (i.e., n % 2 == 0).
- After the loop, check if n is equal to 1. If it is, return true because n has been reduced to 1, which is a power of 2.
- If n is not 1 after the loop, return false because it means that n is not a power of 2.

# Complexity

- Time complexity:

  - The time complexity of this code is O(log n), where n is the input integer. The while loop divides n by 2 repeatedly, which takes logarithmic time in terms of n

- Space complexity:
  - The space complexity is O(1) because the code uses a fixed amount of space to store variables and does not rely on data structures that grow with the input.

# Code

```java
class Solution {
    public boolean isPowerOfTwo(int n) {
        if(n == 0 ) return false;
        while(n % 2 == 0){
            n = n/2;
        }
        if(n == 1) return true;
        return false;
    }
}
```
