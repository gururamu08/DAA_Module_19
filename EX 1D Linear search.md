# EX 1D Linear search
## DATE:16/05/25
## AIM:
Write a python program for a search function with parameter list name and the value to be searched on the given list of int values.




## Algorithm
1. Get the number of items and store them in a list.

2.Ask the user for the search key (the item to find).

3.Check each item one by one in the list.

4.If the key is found, return its position.

5.Print "Found" or "Not Found" based on the result.
## Program:
```
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: GURUMOORTHI R
Register Number:  212222230042
```
```python
def search(List,n):
    for i in range(0,n):
        if(List[i]==key):
            return i
    return -1
List=[]
n=int(input())
for i in range(n):
    List.append((input()))
key=(input())
res=search(List,n)
if(res==-1):
    print("Not Found")
else:
    print("Found")
```

## Output:

![image](https://github.com/user-attachments/assets/8bce594d-5dba-4226-a3a5-3657b3fb41cf)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
