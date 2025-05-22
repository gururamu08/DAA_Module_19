# EX 1B Merge Sort
## DATE:16/5/25
## AIM:
Write a python program to implement merge sort without using recursive function on the given list of values.

## Algorithm
1.Get numbers from the user and store them in a list.

2.Start sorting small parts of the list (2 elements at a time).

3.Use the merge function to combine and sort these small parts.

4.Keep doubling the part size and merging until the whole list is sorted.

5.Print the sorted list at the end.
## Program:
```
Program to implement Merge Sort
Developed by: GURUMOORTHI R
Register Number: 212222230042
```
```python

def mergeSort(a):
    width = 1
    n = len(a)
    while width < n:
        l = 0
        while l < n:
            r = min(l + (width * 2 - 1), n - 1)
            m = min(l + width - 1, n - 1)
            			 
            merge(a, l, m, r)
            l += width * 2
        
        width *= 2
    return a


def merge(a, l, m, r): 
    n1 = m - l + 1
    n2 = r - m 
    L = [0] * n1 
    R = [0] * n2 
    for i in range(0, n1): 
        L[i] = a[l + i] 
    for i in range(0, n2): 
        R[i] = a[m + i + 1] 

    i, j, k = 0, 0, l 
    
    print("left: ",L)
    print("Right: ",R)
    
    while i < n1 and j < n2: 
        if L[i] <= R[j]: 
            a[k] = L[i] 
            i += 1
        else: 
            a[k] = R[j] 
            j += 1
        k += 1

    while i < n1: 
        a[k] = L[i] 
        i += 1
        k += 1

    while j < n2: 
        a[k] = R[j] 
        j += 1
        k += 1

 
n = int(input())
a = []
for i in range(n):
    a.append(int(input()))

mergeSort(a) 
print(a) 

```

## Output:

![image](https://github.com/user-attachments/assets/fe72e42c-7d07-4c15-a387-2c9e0ec22ad7)


## Result:

The program successfully sorts the list using iterative merge sort.
