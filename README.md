Rearrange the array in Python
Here, on this page will learn how to solve Rearrange the array in alternating positive and negative items with O(1) extra space in Python programing language. In O(n) time complexity.

Example:

Input :  [ 7, 5, -2, 1, -3 ]
Output :  [ -2, 5, -3, 1, 7 ]
Rearrange the array in Python

Algorithm
Initialize two variable p, b with value 0
Run a for loop from 0 to length of array using variable i
For each iteration if b is equals to 1 then make b equals to -1
else if arr[i] is less then zero
Swap values of arr[i] & arr[p]
If p is greater then i increment the value of b by 1
Increment value of p by 2
After loop ends print arr
Time And Space Complexity :
Time – Complexity : O(N)
Space – Complexity : O(1)
Python Program to rearrange array
Run
def rearrange(arr):
    p = 0
    b = 0
    for i in range(len(arr)):
        if b == 1:
            b -= 1
        elif arr[i] < 0:
            arr[i], arr[p] = arr[p], arr[i]
            if p > i:
                b += 1
            p += 2
    return arr


array = [2, 3, -4, -1, 6, -9]
print("After Rearranging :", rearrange(array))
