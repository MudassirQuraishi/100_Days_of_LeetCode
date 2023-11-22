---

# 1. Two Sum Problem

Given an array of integers `nums` and an integer `target`, the task is to find indices of the two numbers such that they add up to the `target`.

## Problem Description

You're provided an array `nums` containing integers and an integer `target`. The goal is to return the indices of two numbers from the array such that they sum up to the `target`. It's assumed that each input has exactly one solution, and the same element cannot be used twice to achieve the target sum.

### Examples:

#### Example 1:

```plaintext
Input: nums = [2, 7, 11, 15], target = 9
Output: [0, 1]
Explanation: nums[0] + nums[1] equals 9, so the indices of these numbers are [0, 1].
```

#### Example 2:

```plaintext
Input: nums = [3, 2, 4], target = 6
Output: [1, 2]
Explanation: nums[1] + nums[2] equals 6, so the indices of these numbers are [1, 2].
```

#### Example 3:

```plaintext
Input: nums = [3, 3], target = 6
Output: [0, 1]
Explanation: nums[0] + nums[1] equals 6, so the indices of these numbers are [0, 1].
```

### Constraints:

- The length of `nums` array will be between 2 and 10^4 (inclusive).
- The values of elements in `nums` will be between -10^9 and 10^9 (inclusive).
- The `target` value will be between -10^9 and 10^9 (inclusive).
- Only one valid solution exists.

---

## Question

- Solve it on LeetCode

[Two_Sum](https://leetcode.com/problems/two-sum/description/)
