# EX 1A recursive function
## DATE:16/05/25
## AIM:
Write a Python Program Using a recursive function to calculate the sum of a sequence

## Algorithm
1.Get a number from the user.

2.Check if the number is negative – if yes, tell the user to enter a positive number.

3.Create a function that adds numbers from n down to 1 using recursion.

4.Use the function to calculate the sum if the number is positive.

5.Show the result to the user. 

## Program:
```
Python Program Using a recursive function to calculate the sum of a sequence
Developed by: GURUMOORTHI R
Register Number:  212222230042
```
```python
def recur_sum(n):
   if n <= 1:
       return n
   else:
       return n + recur_sum(n-1)


num = int(input())

if num < 0:
   print("Enter a positive number")
else:
   print(recur_sum(num))
```
## Output:

![image](https://github.com/user-attachments/assets/e49b81fa-93cb-4d29-9ab9-0072b7a93f81)


## Result:

The program successfully calculates the sum of a sequence using recursion.
