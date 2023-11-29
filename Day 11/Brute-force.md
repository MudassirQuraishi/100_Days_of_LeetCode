Certainly! Let's break down the provided solution into its components and add the required information.

---

# Intuition

The initial thought process might involve leveraging a sorting technique to arrange the squares of the given numbers in ascending order.

# Approach

The approach taken here uses a selection sort technique. It iterates through the array, finding the index of the minimum element's square within the unsorted portion. It swaps this minimum element's square with the element at the current index in the iteration, effectively sorting the squares in ascending order. Finally, the method squares each element to match the problem's requirements.

# Complexity

-   Time complexity: $$O(n^2)$$

    -   The solution involves two nested loops. The first loop iterates through the array (`n` elements), and the second loop also iterates through the remaining unsorted portion of the array, resulting in a quadratic time complexity.

-   Space complexity: $$O(1)$$
    -   The space complexity remains constant as the algorithm operates directly on the input array without using additional space proportional to the input size.

# Code

```java
class Solution {
    public int[] sortedSquares(int[] nums) {
        for (int i = 0; i < nums.length; i++) {
            int minIndex = i;
            for (int j = i; j < nums.length; j++) {
                if (Math.pow(nums[j], 2) < Math.pow(nums[minIndex], 2)) {
                    minIndex = j;
                }
            }
            int temp = nums[i];
            nums[i] = nums[minIndex];
            nums[minIndex] = temp;
        }
        for (int i = 0; i < nums.length; i++) {
            nums[i] = nums[i] * nums[i];
        }
        return nums;
    }
}
```

Although this solution effectively sorts the squares, it does so in a less efficient manner compared to certain optimized algorithms due to its quadratic time complexity. Now check for the optimised solution to solve it in linear time complexity.
