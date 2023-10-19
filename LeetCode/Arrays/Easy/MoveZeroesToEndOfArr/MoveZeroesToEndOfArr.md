##### Leetcode 283. Move Zeroes

Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Note that you must do this in-place without making a copy of the array.

***Example 1:***

Input: nums = [0,1,0,3,12]
Output: [1,3,12,0,0]

***Example 2:***

Input: nums = [0]
Output: [0]
___________________________________________________________________________________

***Example***
##### Input
![Alt text](image.png)
##### Output
![Alt text](image-1.png)

____________________________________________________________________________________

```
// console.log("Hello, World!");

// Function which pushes all zeros to end of an array.  
function pushZerosToEnd(arr, n)  
{  
    let nz = 0; // Count of non-zero elements  
  
    // Traverse the array. If element encountered is non-  
    // zero, then replace the element at index 'count'  
    // with this element  
    for (let i = 0; i < n; i++)  
        if (arr[i] != 0)  
            arr[nz++] = arr[i]; // here count is  
                                // incremented  
  
    // Now all non-zero elements have been shifted to  
    // front and 'count' is set as index of first 0.  
    // Make all elements 0 from count to end.  
    while (nz < n)  
        arr[nz++] = 0;  
        
    return arr;
}  
  
// Driver code 
    let arr = [1, 9, 8, 4, 0, 0, 2, 7, 0, 6, 0, 9];  
    let n = arr.length;  
    console.log(pushZerosToEnd(arr, n)); 
```