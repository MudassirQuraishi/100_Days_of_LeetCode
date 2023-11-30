---

# Intuition

The initial intuition appears to be removing all occurrences of a given value `val` from an integer array.

# Approach

The approach utilized here employs a two-pointer technique. The idea is to maintain one pointer (`index`) to keep track of the next available position to place elements that are not equal to the given `val`. As the loop iterates through the array, if the current element is not equal to `val`, it gets placed at the `index` position. The `index` is then incremented to prepare for the next eligible element. The final result would be the count of non-`val` elements till `index`.

# Complexity

-   Time complexity: $$O(n)$$

    -   The solution involves a single pass through the array (`n` elements), where each element is checked only once and copied to the modified array if it's not equal to `val`.

-   Space complexity: $$O(1)$$
    -   The space complexity remains constant as the algorithm operates directly on the input array without utilizing additional space proportional to the input size.

# Code

```java
class Solution {
    public int removeElement(int[] nums, int val) {
        int index = 0;
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] != val) {
                nums[index++] = nums[i];
            }
        }
        return index;
    }
}
```

This solution effectively removes occurrences of the given value `val` from the array and returns the count of elements remaining after the removal process. The algorithm performs this operation in linear time complexity without using extra space.
