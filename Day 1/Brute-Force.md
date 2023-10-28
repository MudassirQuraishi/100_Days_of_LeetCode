# Intuition

The intuition behind this code is to first convert the given integer to a string, making it easier to compare the characters. Then, it iterates through the first half of the string while comparing characters from the beginning and end of the string. If all character comparisons are equal, the number is considered a palindrome.

# Approach

- Convert the integer to a string.
- Find the length of the string (the number of digits).
- Iterate through the first half of the string and compare characters from the beginning and end.

# Complexity

- Time complexity:

  - The code iterates through the first half of the string, which is directly proportional to the number of digits.

- Space complexity:
  - The space used is mainly for the string representation of the integer, which also depends on the number of digits in the integer.

# Code

```
class Solution {
    public boolean isPalindrome(int x) {
        String s = String.valueOf(x);
        int n = s.length();
        for(int i = 0; i < n/2; i++){
            if(s.charAt(i)!= s.charAt(n-1-i)) return false;
        }
        return true;
    }
}
```
