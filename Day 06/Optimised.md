# Intuition

The problem aims to find two numbers in an array that sum up to a given target value.

# Approach

1. **HashMap for Efficient Lookup:** The code uses a HashMap to efficiently track elements and their corresponding indices in the array.
2. **Finding Complements:** For each element `nums[i]`, it calculates the complementary value `comp` required to reach the `target` sum.
3. **Checking Complements:** It checks if the HashMap already contains the complement. If it does, it means the current number plus a previous number in the array reaches the target, and it returns their indices.
4. **Storing Elements:** If the complement is not found, it stores the current number and its index in the HashMap for potential future use.

# Complexity

- Time complexity:
  - The time complexity of this solution is O(n), where n is the number of elements in the `nums` array. It iterates through the array once, and each lookup in the HashMap is on average O(1).
- Space complexity:
  - The space complexity is O(n) as well. The HashMap can potentially store all elements in the `nums` array in the worst-case scenario.

# Code

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int initialCapacity = (int) (nums.length / 0.75);
        HashMap<Integer, Integer> map = new HashMap<>(initialCapacity);

        for (int i = 0; i < nums.length; i++) {
            int comp = target - nums[i];
            if (map.containsKey(comp)) {
                return new int[]{map.get(comp), i};
            }
            map.put(nums[i], i);
        }
        return new int[]{-1, -1};
    }
}

```
