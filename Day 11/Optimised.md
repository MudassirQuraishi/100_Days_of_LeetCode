---

# Intuition

Given a sorted array of integers, the goal is to square each element and return the resulting array in sorted order.

# Approach

The approach here utilizes a two-pointer technique to traverse the input array in a way that maintains the sorted order of squares. We start by initializing two pointers at the beginning and end of the input array. By comparing the absolute values of elements at these pointers, we fill the result array from the end to the start, ensuring the largest squares are placed at the end and gradually filling towards the beginning.

# Complexity

-   Time complexity: $$O(n)$$
    -   The solution involves a single pass through the input array, performing constant time operations within the loop.
-   Space complexity: $$O(n)$$
    -   An additional array of size `n` is used to store the squared elements.

# Code

```java
class Solution {
    public int[] sortedSquares(int[] nums) {
        int[] result = new int[nums.length];
        int left = 0;
        int right = nums.length - 1;

        for (int i = nums.length - 1; i >= 0; i--) {
            if (Math.abs(nums[left]) > Math.abs(nums[right])) {
                result[i] = nums[left] * nums[left];
                left++;
            } else {
                result[i] = nums[right] * nums[right];
                right--;
            }
        }

        return result;
    }
}
```
