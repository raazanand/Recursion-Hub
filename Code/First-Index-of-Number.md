---
Name: 'Pratibha Singh'
Github: 'https://github.com/Crazy2code15'
WebSite: 
Problem: 'First Index of Number'
Description: 'Find First Index of Number using recursion.'
Explanation: 'Given an array of length N and an integer x, you need to find and return the first index of integer x present in the array. Return -1 if it is not present in the array.'
Language: 'Python' 
---

```py
def firstIndex(arr, x):
    l = len(arr)
    if l == 0:
        return -1
    
    if arr[0] == x:
        return 0
    
    smallerList = arr[1:]
    smallerListOutput = firstIndex(smallerList, x)
    if smallerListOutput == -1:
        return -1
    else:
        return smallerListOutput + 1

# Main
from sys import setrecursionlimit
setrecursionlimit(11000)
n=int(input())
arr=list(int(i) for i in input().strip().split(' '))
x=int(input())
print(firstIndex(arr, x))
```
