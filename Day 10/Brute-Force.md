# Intuition

Initially, the aim was to find a missing number within an array.

# Approach

We tackled this by utilizing a HashSet to track unique elements in the array. Then, by iterating through a range from 1 to the array's length, we identified the missing number by checking for its absence in the HashSet.

# Complexity

-   Time complexity:
    The time complexity here is O(n), where n represents the array's length. This complexity arises due to iterating through the array and HashSet operations.

-   Space complexity:
    The space complexity is O(n) as we use a HashSet to store unique elements from the array, potentially occupying space proportional to the array's size.

# Code

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n = nums.length;
        int missingNumber = 0;
        HashSet<Integer> uniqueSet = new HashSet <>();
        for(int element : nums){
            uniqueSet.add(element);
        }
        for(int i = 1; i <= n; i++){
            if(!uniqueSet.contains(i)){
                missingNumber = i;
                break;
            }
        }
        return missingNumber;
    }
}
```
