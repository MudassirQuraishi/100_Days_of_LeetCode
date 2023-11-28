# Intuition

So, we wanted to find a missing number in an array. The idea was to use a cool math trick called the XOR operation to solve this.

# Approach

What we did was loop through the array, performing XOR between each array element and its respective index. This XOR operation helps cancel out the numbers that are present in the array at their correct positions.

# Complexity

-   Time complexity:
    The time it takes to find the missing number is pretty neat, just O(n) where n is the array's length. We loop through the array once, doing some quick operations each time.

-   Space complexity:
    We're smart about space here, just O(1). We don't use any extra space that grows with the input size; it's all about using the variables we have.

# Code

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n = nums.length;
        int missingNumber = n;

        for (int i = 0; i < n; i++) {
            missingNumber ^= i ^ nums[i];
        }

        return missingNumber;
    }
}
```

So, that's how we used this XOR trick to find the missing number. It's a quick and space-efficient way to solve this problem!
