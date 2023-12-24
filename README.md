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
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
'''
Program for linear search method to match the item in a list
Developed by: K Kesava sai
RegisterNumber: 212223230105
'''
def linearSearch(array,n,k):
    for i in range (n) :
        if array [i] ==k :
            return i
    return -1        
array = eval(input())
array.sort ()
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len (array)
print (array)
result = linearSearch (array,n,k)
if result ==-1 :
    print ("Element not found")
else:
    print("Element found at index: ",result)




```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: K Kesava sai
RegisterNumber: 212223230105
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array [mid]==k:
            return mid
        elif array [mid]<k:
            low = mid+1
        else:
            high=mid-1
    return -1        
array = eval(input())
array.sort()
k = eval(input()) 
print(array)
result=binarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: K Kesava sai
RegisterNumber: 212223230105
'''
def BinarySearch(arr, k, low, high):
    if low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr [mid]<k:
            return BinarySearch(arr, k, mid+1, high)
        else:
            return BinarySearch(arr, k, low, mid-1)
    else:
        return -1
arr = eval(input())
arr.sort()
print (arr)
k = eval(input()) # k is the element to be searched for
result=BinarySearch(arr, k,0,len(arr)-1)
# use the binary search function to find the result
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)



```
## Sample Input and Output
(i)
![phy-3b-1](https://github.com/Kesavasai20/Search-Algorithm/assets/138849303/aca8aaf7-9736-4339-8b74-c9fd336b6f55)
(ii)
![phy-3b-2](https://github.com/Kesavasai20/Search-Algorithm/assets/138849303/cb97d358-09ea-46a5-9f41-64fe67c0e29b)
(iii)
![phy-3b-3](https://github.com/Kesavasai20/Search-Algorithm/assets/138849303/26bc6ee4-13f1-4743-b3b9-18a59c4ecc21)





## Result
Thus the linear search and binary search algorithm is implemented using python programming.
