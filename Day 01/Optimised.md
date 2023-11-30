# Intuition

Our first thought is to reverse the number and check if the reversed number is equal to the original. If they match, it's a palindrome.

# Approach

- If the input number is negative, it can't be a palindrome. We return false in this case.
- Initialize two variables, "reversed" and "temp," both initially set to x.
- Reverse the number by repeatedly extracting the last digit of "temp" and adding it to the "reversed" number.
- Continue this process until "temp" becomes zero.
- After the loop, "reversed" holds the reversed number.
- Check if the reversed number is equal to the original "x," which determines if the number is a palindrome.

# Complexity

- **Time complexity:** The while loop runs for each digit of the number, so the time complexity is O(n), where n is the number of digits in x.
- **Space complexity:** We use a constant amount of extra space, so the space complexity is O(1).

# Code

``` java
class Solution {
    public boolean isPalindrome(int x) {
        if (x < 0) {
            return false;
        }
        int reversed = 0;
        int temp = x;
        while(temp != 0){
            int digit = (int) (temp % 10);
            reversed = reversed * 10 + digit;
            temp /= 10;
        }
        return (reversed == x);
    }
}
```
