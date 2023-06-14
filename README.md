# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid.
5.	This is done by setting low to low = mid + 1.
6.	Else, compare x with the middle element of the elements on the left side of mid.
7.  This is done by setting high to high = mid - 1.
8.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Shalini.k
RegisterNumber: 212222240095
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
array.sort()
result = linearSearch(array,n,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list 
otherwise print sorted array and "Element found at index: ", result
if (result==-1):
    print(array,"\nElement not found")
else:
    print(array,"\nElement found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Shalini.k
RegisterNumber: 212222240095
'''
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above 
    or below the middle value
    while low<=high:
        mid = low+(high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid]<k:
            low = mid+1
        else:
            high = mid -1
    return -1
array = eval(input())
# sort the array
array.sort()
k = eval(input()) #k-item to be searched
# use the binary search function to find the item in the list
# use if-else to print sorted array and "Element not found" if the item is not present in the list 
otherwise print sorted array and "Element found at index: ", result
result= binarySearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array,"\nElement not found")
else:
    print(array,"\nElement found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Shalini.k
RegisterNumber: 212222240095
'''
def BinarySearch(arr, k, low, high):
    # Write your code here for binary search using recursive method
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr, k, mid+1, high)
        else:
            return BinarySearch(arr, k, low,mid-1)
    return -1
arr = eval(input())
arr.sort()
#sort the array
k = eval(input()) # k is the element to be searched for
result= BinarySearch(arr,k,0,len(arr)-1)
# use the binary search function to find the result
# use if-else to print sorted array and "Element not found" if the item is not present in the list 
otherwise print sorted array and "Element found at index: ", result
if(result==-1):
    print(arr,"\nElement not found")
else:
    print(arr,"\nElement found at index: ",result)
```
## Sample Input and Output
![Screenshot (138)](https://github.com/shalinikannan23/Search-Algorithm/assets/118656529/b7ec37d7-010d-4d2f-b442-d86bba9baab9)
![Screenshot (139)](https://github.com/shalinikannan23/Search-Algorithm/assets/118656529/7993a130-5240-47d6-9a11-07dea702663b)
![Screenshot (140)](https://github.com/shalinikannan23/Search-Algorithm/assets/118656529/6f883105-278b-4dce-b619-988b4f4e25c1)
## Result
Thus the linear search and binary search algorithm is implemented using python programming.
