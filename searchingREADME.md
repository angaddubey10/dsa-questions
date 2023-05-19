# SEARCHING AND SORTING
# SEARCHING
## **Searching an element in a sorted array**
## **Left Index**
## **Peak element**
## **Count 1's in binary array**
## **Floor in a Sorted Array**
## **Search an Element in an array**

---
# SORTING

## **Bubble Sort**
## **Insertion Sort**
## **Count Inversions**
## **Quick Sort**
## **Binary Array Sorting**

---
# SEARCHING

<details>
<summary>Searching an element in a sorted array
 </summary>
  
      Dificulty Level : Basic
  Given an array arr[] sorted in ascending order of size N and an integer K. Check if K is present in the array or not.


Example 1:

Input:
N = 5, K = 6
arr[] = {1,2,3,4,6}
Output: 1
Exlpanation: Since, 6 is present in 
the array at index 4 (0-based indexing),
output is 1.
 

Example 2:

Input:
N = 5, K = 2
arr[] = {1,3,4,5,6}
Output: -1
Exlpanation: Since, 2 is not present 
in the array, output is -1.
 

Your Task:
You don't need to read input or print anything. Complete the function searchInSorted() which takes the sorted array arr[], its size N and the element K as input parameters and returns 1 if K is present in the array, else it returns -1. 


Expected Time Complexity: O(Log N)
Expected Auxiliary Space: O(1)

 

Constraints:
1 <= N <= 106
1 <= K <= 106
1 <= arr[i] <= 106

```python
 #User function Template for python3

class Solution:
    ##Complete this function
    def searchInSorted(self,arr, N, K):
        #Your code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3

import math
if __name__ == '__main__': 
	t = int(input())
	for _ in range(t):
		NK = input().strip().split()
		N = int(NK[0])
		K = int(NK[1])
		A = [ int(x) for x in input().strip().split() ]
		ob=Solution()
		print(ob.searchInSorted(A,N,K))

# } Driver Code Ends
```
</details>

<details>
<summary> Left Index
</summary>
  
    Dificulty Level : Basic
Given a sorted array of integers of size N and a number X. Find the leftmost index of X in the array arr[].

Example 1:

Input:
N = 10
arr[] = {1, 1, 2, 2, 3, 4, 5, 5, 6, 7}
X = 1
Output: 0 
Explanation: Because the element 1   
appears twice and its left most 
occurrence is at index 0.

Example 2:

Input:
N = 5
arr[] = {2, 2, 3, 3, 4}
X = 4
Output: 4
Explanation: Because element 4 appears 
only once at index 4.

Your Task:  
You don't need to read input or print anything. Your task is to complete the function leftIndex() which takes the array arr[], its size N and an integer X as input parameters and returns the leftmost occurrence of X in arr[]. If X is not present in the array, return -1.

Expected Time Complexity: O(LogN)
Expected Auxiliary Space: O(1)

Constraints:
1 <= N <= 106
-105 <= arr[i] <= 105
Array may contain duplicate elements.   
  

```python
#User function Template for python3

class Solution:
    def leftIndex (self, N, arr, X):
        # code here 
        
        


#{ 
 # Driver Code Starts
#Initial Template for Python 3

if __name__ == '__main__': 
    t = int (input ())
    for _ in range (t):
        N = int(input())
        arr = input().split()
        for itr in range(N):
            arr[itr] = int(arr[itr])
        X = int(input())

        ob = Solution()
        print(ob.leftIndex(N, arr, X))

# } Driver Code Ends  
```

</details>

<details>
<summary> Peak element
</summary>
  
    Dificulty Level : Basic
  
An element is called a peak element if its value is not smaller than the value of its adjacent elements(if they exists).
Given an array arr[] of size N, Return the index of any one of its peak elements.
Note: The generated output will always be 1 if the index that you return is correct. Otherwise output will be 0. 


Example 1:

Input: 
N = 3
arr[] = {1,2,3}
Possible Answer: 2
Generated Output: 1
Explanation: index 2 is 3.
It is the peak element as it is 
greater than its neighbour 2.
If 2 is returned then the generated output will be 1 else 0.
Example 2:

Input:
N = 3
arr[] = {3,4,2}
Possible Answer: 1
Output: 1
Explanation: 4 (at index 1) is the 
peak element as it is greater than 
it's neighbor elements 3 and 2.
If 1 is returned then the generated output will be 1 else 0.
 

Your Task:
You don't have to read input or print anything. Complete the function peakElement() which takes the array arr[] and its size N as input parameters and return the index of any one of its peak elements.

Can you solve the problem in expected time complexity?

 

Expected Time Complexity: O(log N)
Expected Auxiliary Space: O(1)


Constraints:
1 ≤ N ≤ 105
1 ≤ A[] ≤ 106  

```python
# your task is to complete this function
# function should return index to the any valid peak element
class Solution:   
    def peakElement(self,arr, n):
        # Code here



#{ 
 # Driver Code Starts
if __name__=='__main__':
    t = int(input())
    for i in range(t):
        n = int(input())
        arr = list(map(int, input().strip().split()))
        index = Solution().peakElement(arr.copy(), n)
        flag = False
        if index<0 or index>=n:
            flag = False
        else:
            if index == 0 and n==1:
                flag = True
            elif index==0 and arr[index]>=arr[index+1]:
                flag = True
            elif index==n-1 and arr[index]>=arr[index-1]:
                flag = True
            elif arr[index-1] <= arr[index] and arr[index] >= arr[index+1]:
                flag = True
            else:
                flag = False

        if flag:
            print(1)
        else:
            print(0)
# Contributed by: Harshit Sidhwa

# } Driver Code Ends  
```

</details>


<details>
<summary> Count 1's in binary array
</summary>
  
    Dificulty Level : Basic
Given a binary sorted non-increasing array of 1s and 0s. You need to print the count of 1s in the binary array.

Example 1:

Input:
N = 8
arr[] = {1,1,1,1,1,0,0,0}
Output: 5
Explanation: Number of 1's in given 
binary array : 1 1 1 1 1 0 0 0 is 5.
Example 2:

Input:
N = 8
arr[] = {1,1,0,0,0,0,0,0}
Output: 2
Explanation: Number of 1's in given 
binary array : 1 1 0 0 0 0 0 0 is 2.
Your Task:
The task is to complete the function countOne() which takes the array arr[] and its size N as inputs and returns the count of 1s in the input array.

Expected Time Complexity: O(LogN).
Expected Auxiliary Space: O(1).

Constraint:
1 <= N <= 5*106
arr[i] = 0,1  
  

```python
#User function Template for python3

class Solution:
    ##Complete this code
    def countOnes(self,arr, N):
        #Your code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3

import math


def main():
        T=int(input())
        while(T>0):
            
            N=int(input())

            A=[int(x) for x in input().strip().split()]
            
            
            ob=Solution()
            print(ob.countOnes(A,N))
            
            T-=1


if __name__ == "__main__":
    main()
# } Driver Code Ends  
```

</details>

<details>
<summary> Floor in a Sorted Array
</summary>
  
    Dificulty Level : Basic
Given a sorted array arr[] of size N without duplicates, and given a value x. Floor of x is defined as the largest element K in arr[] such that K is smaller than or equal to x. Find the index of K(0-based indexing).

Example 1:

Input:
N = 7, x = 0 
arr[] = {1,2,8,10,11,12,19}
Output: -1
Explanation: No element less 
than 0 is found. So output 
is "-1".
Example 2:

Input:
N = 7, x = 5 
arr[] = {1,2,8,10,11,12,19}
Output: 1
Explanation: Largest Number less than 5 is
2 (i.e K = 2), whose index is 1(0-based 
indexing).
Your Task:
The task is to complete the function findFloor() which returns an integer denoting the index value of K or return -1 if there isn't any such number.

Expected Time Complexity: O(log N).
Expected Auxiliary Space: O(1).

Constraints:
1 ≤ N ≤ 107
1 ≤ arr[i] ≤ 1018
0 ≤ X ≤ arr[n-1]  
  

```python
class Solution:
    #User function Template for python3
    
    #Complete this function
    def findFloor(self,A,N,X):
        #Your code here
        


#{ 
 # Driver Code Starts
#Initial Template for Python 3


import math


def main():
        T=int(input())
        while(T>0):
            
            NX=[int(x) for x in input().strip().split()]
            N=NX[0]
            X=NX[1]

            A=[int(x) for x in input().strip().split()]
            
            obj = Solution()
            print(obj.findFloor(A,N,X))
            
            T-=1


if __name__ == "__main__":
    main()
# } Driver Code Ends  
```

</details>

<details>
<summary> Search an Element in an array
</summary>
  
    Dificulty Level : Basic
Given an integer array and another integer element. The task is to find if the given element is present in array or not.

Example 1:

Input:
n = 4
arr[] = {1,2,3,4}
x = 3
Output: 2
Explanation: There is one test case 
with array as {1, 2, 3 4} and element 
to be searched as 3.  Since 3 is 
present at index 2, output is 2.
Example 2:

Input:
n = 5
arr[] = {1,2,3,4,5}
x = 5
Output: 4
Explanation: For array elements 
{1,2,3,4,5} element to be searched 
is 5 and it is at index 4. So, the 
output is 4.
Your Task:
The task is to complete the function search() which takes the array arr[], its size N and the element X as inputs and returns the index of first occurrence of X in the given array. If the element X does not exist in the array, the function should return -1.

Expected Time Complexity: O(n).
Expected Auxiliary Space: O(1). 

Constraints:
1 <= n <= 106
0 <= arr[i] <= 106
0 <= x <= 105  
  

```python
#User function Template for python3

class Solution:
    #Complete the below function
    def search(self,arr, N, X):
        #Your code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3


import math



    
def main():
        T=int(input())
        while(T>0):
            
            N=int(input())
            
            A=[int(x) for x in input().strip().split()]
            
            x=int(input())
            ob=Solution()
            print(ob.search(A,N,x))
            
            T-=1


if __name__ == "__main__":
    main()
# } Driver Code Ends  
```

</details>

---
# SORTING

  
<details>
<summary> Bubble Sort
</summary>
  
    Dificulty Level : Basic
Given an Integer N and a list arr. Sort the array using bubble sort algorithm.
Example 1:

Input: 
N = 5
arr[] = {4, 1, 3, 9, 7}
Output: 
1 3 4 7 9
Example 2:

Input:
N = 10 
arr[] = {10, 9, 8, 7, 6, 5, 4, 3, 2, 1}
Output: 
1 2 3 4 5 6 7 8 9 10

Your Task: 
You don't have to read input or print anything. Your task is to complete the function bubblesort() which takes the array and it's size as input and sorts the array using bubble sort algorithm.

Expected Time Complexity: O(N^2).
Expected Auxiliary Space: O(1).

Constraints:
1 <= N <= 103
1 <= arr[i] <= 103  
  

```python
#User function Template for python3

class Solution:
    #Function to sort the array using bubble sort algorithm.
    def bubbleSort(self,arr, n):
        # code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3



if __name__=='__main__':
    t = int(input())
    for i in range(t):
        n = int(input())
        arr = list(map(int, input().strip().split()))
        ob = Solution()
        ob.bubbleSort(arr, n)
        for i in arr:
            print(i,end=' ')
        print()

# } Driver Code Ends  
```

</details>

<details>
<summary> Insertion Sort
</summary>
  
    Dificulty Level : Basic
The task is to complete the insert() function which is used to implement Insertion Sort.


Example 1:

Input:
N = 5
arr[] = { 4, 1, 3, 9, 7}
Output:
1 3 4 7 9
Example 2:

Input:
N = 10
arr[] = {10, 9, 8, 7, 6, 5, 4, 3, 2, 1}
Output:
1 2 3 4 5 6 7 8 9 10

Your Task: 
You don't have to read input or print anything. Your task is to complete the function insert() and insertionSort() where insert() takes the array, it's size and an index i and insertionSort() uses insert function to sort the array in ascending order using insertion sort algorithm. 

Expected Time Complexity: O(N*N).
Expected Auxiliary Space: O(1).


Constraints:
1 <= N <= 1000
1 <= arr[i] <= 1000  
  

```python
#Sort the array using insertion sort

class Solution:
    def insert(self, alist, index, n):
        #code here
        
    #Function to sort the list using insertion sort algorithm.    
    def insertionSort(self, alist, n):
        #code here


#{ 
 # Driver Code Starts
if __name__=="__main__":
    t=int(input())
    for i in range(t):
        n=int(input())
        arr=list(map(int,input().split()))
    
        Solution().insertionSort(arr,n)
    
        for i in range(n):
            print(arr[i],end=" ")
    
        print()
# } Driver Code Ends  
```

</details>

<details>
<summary> Count Inversions
</summary>
  
    Dificulty Level : Basic
Given an array of integers. Find the Inversion Count in the array. 

Inversion Count: For an array, inversion count indicates how far (or close) the array is from being sorted. If array is already sorted then the inversion count is 0. If an array is sorted in the reverse order then the inversion count is the maximum. 
Formally, two elements a[i] and a[j] form an inversion if a[i] > a[j] and i < j.
 

Example 1:

Input: N = 5, arr[] = {2, 4, 1, 3, 5}
Output: 3
Explanation: The sequence 2, 4, 1, 3, 5 
has three inversions (2, 1), (4, 1), (4, 3).
Example 2:

Input: N = 5
arr[] = {2, 3, 4, 5, 6}
Output: 0
Explanation: As the sequence is already 
sorted so there is no inversion count.
Example 3:

Input: N = 3, arr[] = {10, 10, 10}
Output: 0
Explanation: As all the elements of array 
are same, so there is no inversion count.
Your Task:
You don't need to read input or print anything. Your task is to complete the function inversionCount() which takes the array arr[] and the size of the array as inputs and returns the inversion count of the given array.'

Expected Time Complexity: O(NLogN).
Expected Auxiliary Space: O(N).

Constraints:
1 ≤ N ≤ 5*105
1 ≤ arr[i] ≤ 1018  
  

```python
class Solution:
    #User function Template for python3
    
    # arr[]: Input Array
    # N : Size of the Array arr[]
    #Function to count inversions in the array.
    def inversionCount(self, arr, n):
        # Your Code Here


#{ 
 # Driver Code Starts
#Initial Template for Python 3

import atexit
import io
import sys

_INPUT_LINES = sys.stdin.read().splitlines()
input = iter(_INPUT_LINES).__next__
_OUTPUT_BUFFER = io.StringIO()
sys.stdout = _OUTPUT_BUFFER

@atexit.register

def write():
    sys.__stdout__.write(_OUTPUT_BUFFER.getvalue())

if __name__=='__main__':
    t = int(input())
    for tt in range(t):
        n = int(input())
        a = list(map(int, input().strip().split()))
        obj = Solution()
        print(obj.inversionCount(a,n))
# } Driver Code Ends  
```

</details>

<details>
<summary> Quick Sort
</summary>
  
    Dificulty Level : Basic
Quick Sort is a Divide and Conquer algorithm. It picks an element as a pivot and partitions the given array around the picked pivot.
Given an array arr[], its starting position is low (the index of the array) and its ending position is high(the index of the array).

Note: The low and high are inclusive.

Implement the partition() and quickSort() functions to sort the array.


Example 1:

Input: 
N = 5 
arr[] = { 4, 1, 3, 9, 7}
Output:
1 3 4 7 9
Example 2:

Input: 
N = 9
arr[] = { 2, 1, 6, 10, 4, 1, 3, 9, 7}
Output:
1 1 2 3 4 6 7 9 10

Your Task: 
You don't need to read input or print anything. Your task is to complete the functions partition()  and quickSort() which takes the array arr[], low and high as input parameters and partitions the array. Consider the last element as the pivot such that all the elements less than(or equal to) the pivot lie before it and the elements greater than it lie after the pivot.


Expected Time Complexity: O(N*logN)
Expected Auxiliary Space: O(logN)


Constraints:
1 <= N <= 103
1 <= arr[i] <= 104  
  

```python
#User function Template for python3

class Solution:
    #Function to sort a list using quick sort algorithm.
    def quickSort(self,arr,low,high):
        # code here
    
    def partition(self,arr,low,high):
        # code here
    


#{ 
 # Driver Code Starts
#Initial Template for Python 3

if __name__ == "__main__":
    t=int(input())
    for i in range(t):
        n=int(input())
        arr=list(map(int,input().split()))
        Solution().quickSort(arr,0,n-1)
        for i in range(n):
            print(arr[i],end=" ")
        print()

# } Driver Code Ends  
```

</details>

<details>
<summary> Binary Array Sorting
</summary>
  
    Dificulty Level : Basic
Given a binary array A[] of size N. The task is to arrange the array in increasing order.
Note: The binary array contains only 0  and 1.
 

Example 1:

Input: 
5
1 0 1 1 0

Output: 
0 0 1 1 1

Explanation: 
After arranging the elements in 
increasing order, elements will be as 
0 0 1 1 1.
Example 2:

Input:
10
1 0 1 1 1 1 1 0 0 0

Output: 
0 0 0 0 1 1 1 1 1 1

Explanation: 
After arranging the elements in 
increasing order, elements will be 
0 0 0 0 1 1 1 1 1 1.

Your Task: This is a function problem. You only need to complete the function binSort() that takes the array A[] and it's size N as parameters and sorts the array. The printing is done automatically by the driver code.

Expected Time Complexity: O(N)
Expected Auxilliary Space: O(1)

Constraints:
1 <= N <= 106
0 <= A[i] <= 1  
  

```python
#User function Template for python3

class Solution:
    
    #Function to sort the binary array.
    def binSort(self, A, N): 
        #Your code here
        #No need to print the array
    


#{ 
 # Driver Code Starts
#Initial Template for Python 3

import math


def main():
        T=int(input())
        while(T>0):
            N=int(input())
            A=list(map(int,input().split()))
            obj = Solution()
            obj.binSort(A,N)
            
            for i in A:
                print(i,end=" ")
            print()
            
            T-=1


if __name__ == "__main__":
    main()
# } Driver Code Ends  
```

</details>


