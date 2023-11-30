## Intuition

This code seems to be tackling the problem of finding the median of two sorted arrays by merging them into a single sorted array and then calculating the median based on the length of the merged array. Here are my thoughts on this. The intuition behind this approach is to merge the two sorted arrays into a single sorted array and then find the median based on the length of the merged array.

## Approach

-   Create a new array to merge the given sorted arrays.
-   Use two pointers (`index1` and `index2`) to iterate through both arrays, comparing elements and merging them into the `mergedArray` in sorted order.
-   After merging, calculate the median based on the length of the merged array:
    -   If the length is odd, the median is the middle element.
    -   If the length is even, the median is the average of the two middle elements.

## Complexity

-   Time complexity: $$O(m + n)$$ where \(m\) and \(n\) are the lengths of the input arrays `num1` and `num2`, respectively. The while loops iterate through both arrays once.
-   Space complexity: $$O(m + n)$$ since an additional array of size `num1.length + num2.length` (`mergedArray`) is created to store the merged elements.

# Code

```java
class Solution {
    public double findMedianSortedArrays(int[] num1, int[] num2) {
        double median = 0;
        int [] mergedArray = new int [num1.length+num2.length];

        int n = mergedArray.length;
        int index = 0;
        int index1 = 0;
        int index2 = 0;
        while(index1 < num1.length && index2 < num2.length){
            if(num1[index1] < num2[index2]){
                mergedArray[index++] = num1[index1++];
            }
            else{
                mergedArray[index++] = num2[index2++];
            }
        }
        while(index1 < num1.length){
            mergedArray[index++] = num1[index1++];
        }
        while(index2 < num2.length){
            mergedArray[index++] = num2[index2++];
        }
        if (mergedArray.length == 1){
            median = mergedArray[0];
            System.out.println(median);
            return median;
        }

        if(n % 2 != 0){
            median = mergedArray[n/2];
        }
        else{
            median =(double) (mergedArray[n/2 -1] + mergedArray[(n/2)]) / 2;
        }
        return median;
    }
}
```
