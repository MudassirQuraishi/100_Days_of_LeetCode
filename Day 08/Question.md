# 1464. Maximum Product of Two Elements in an Array

Given an array of integers `nums`, you need to choose two different indices `i` and `j` from the array. Return the maximum value of `(nums[i]-1) * (nums[j]-1)`.

## Examples

### Example 1

#### Input:

```
nums = [3, 4, 5, 2]
```

#### Output:

```
12
```

#### Explanation:

Choosing the indices `i=1` and `j=2` (indexed from 0), you get the maximum value: `(nums[1]-1) * (nums[2]-1) = (4-1) * (5-1) = 3 * 4 = 12`.

### Example 2

#### Input:

```
nums = [1, 5, 4, 5]
```

#### Output:

```
16
```

#### Explanation:

Choosing the indices `i=1` and `j=3` (indexed from 0), you get the maximum value: `(5-1) * (5-1) = 16`.

### Example 3

#### Input:

```
nums = [3, 7]
```

#### Output:

```
12
```

#### Explanation:

Choosing the indices `i=0` and `j=1` (indexed from 0), you get the maximum value: `(3-1) * (7-1) = 2 * 6 = 12`.

## Constraints

-   2 <= nums.length <= 500
-   1 <= nums[i] <= 10^3

## Question

-   Solve it on LeetCode

[Maximum_Product_of_Two_Elements_in_an_Array](https://leetcode.com/problems/maximum-product-of-two-elements-in-an-array/description/)
