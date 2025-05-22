# EX 1C Quick Sort
## DATE:16/05/25
## AIM:
Write a python program to implement quick sort using tha last element as pivot on the list of float values.


## Algorithm
1.take input numbers from the user and store them in a list.

2.Pick a pivot (the last number in the current part of the list).

3.Rearrange the list so smaller numbers come before the pivot and larger ones after.

4.Repeat the steps (recursively) for the left and right parts of the list.

5.Print the sorted list after sorting is complete. 

## Program:
```
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: GURUMOORTHI R
Register Number:  212222230042
```
```python
def partition(arr, low, high):
    i = (low-1)
    pivot = arr[high]

    for j in range(low, high):
        if arr[j] <= pivot:
            i = i+1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i+1], arr[high] = arr[high], arr[i+1]
    return (i+1)

def quickSort(arr, low, high):
    if len(arr) == 1:
        return arr
    if low < high:
        pi = partition(arr, low, high)
        quickSort(arr, low, pi-1)
        quickSort(arr, pi+1, high)

arr = []
n = int(input())
for i in range (n):
    arr.append(float(input()))
#print("Original array is:")
#for i in arr:
#    print(i)
quickSort(arr, 0, n-1)
print("Sorted array is:")
for i in arr:
    print(i)

```

## Output:


![image](https://github.com/user-attachments/assets/8e493967-f230-4c97-b7c9-7c5606653438)

## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
