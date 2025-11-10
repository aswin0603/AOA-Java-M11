
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 13-08-2025
## AIM:
To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm
1. Start the program and import the `Scanner` class to take user input.
2. Read the sizes of the two sorted arrays and store their elements in `nums1` and `nums2`.
3. Calculate the total length of both arrays combined.
4. Use the `getMin()` method to sequentially retrieve the smallest elements from both arrays until reaching the median position.
5. Display the median value of the merged sorted arrays as the final output. 

## Program:
```java
import java.util.Scanner;

public class Solution {
    private int p1 = 0, p2 = 0;

    private int getMin(int[] nums1, int[] nums2) {
        if (p1 < nums1.length && p2 < nums2.length) {
            return nums1[p1] < nums2[p2] ? nums1[p1++] : nums2[p2++];
        } else if (p1 < nums1.length) {
            return nums1[p1++];
        } else if (p2 < nums2.length) {
            return nums2[p2++];
        }
        return -1; 
    }

    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
       int m = nums1.length, n = nums2.length;
        int[] merged = new int[m + n];
        int i = 0, j = 0, k = 0;

        
        while (i < m && j < n) {
            if (nums1[i] < nums2[j]) {
                merged[k++] = nums1[i++];
            } else {
                merged[k++] = nums2[j++];
            }
        }

        while (i < m) {
            merged[k++] = nums1[i++];
        }
        while (j < n) {
            merged[k++] = nums2[j++];
        }

        int total = m + n;
        if (total % 2 == 1) {
            return merged[total / 2];
        } else {
            return (merged[total / 2 - 1] + merged[total / 2]) / 2.0;
        }

    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Solution sol = new Solution();

        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }

        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        double median = sol.findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);
        
        sc.close();
    }
}

```

## Output:
<img width="854" height="275" alt="image" src="https://github.com/user-attachments/assets/1eea85e8-4e19-4935-acaf-844e15494cac" />



## Result:
The program successfully implemented and the expected output is verified.


```
Developed by: ASWIN B
Register Number:  212224110007
```
