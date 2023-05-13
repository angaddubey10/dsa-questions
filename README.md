# **Recursion Problems**
## **The Sequence**
## **Print 1 To N Without Loop**
## **Print Array Elements Using Recursion**
## **Sum of Digits of a Number**
## **Count Total Digits in a Number**
## **Fibonacci Using Recursion**
## **Factorial Using Recursion**
## **Find nCr**
## **Check Palindrome**
## **Recursively Sum N Numbers**
## **GCD Euclid**

---
<details> <summary> The Sequence </summary>
      
      Dificulty Level : Basic

You are given a number n. You need to recursively find the nth term of the series S that is given by:
      
S(n) = n+ n*(S(n-1)) and S(0) = 1

### Example 1:

  Input: n = 2

  Output: 6

### Example 2:

  Input:
  n = 3

  Output: 21
      
### Your Task:

Complete the function theSequence that takes n as paramenter and return the answer.

Expected Time Complexity: O(N).
Expected Auxiliary Space: O(N) (Recursive).

 Constraints: 
1 <= n <= 10

```python
 #User function Template for python3

def theSequence(n):
    #code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3

#contributed by RavinderSinghPB
if __name__=='__main__':
    tcs=int(input())

    for _ in range(tcs):
        n=int(input())

        print(theSequence(n))
# } Driver Code Ends
```
---
 
</details>


<details>
<summary>
 Print 1 To N Without Loop </summary>
      Dificulty Level : Basic
  
 Print numbers from 1 to N without the help of loops.
### Example 1:
Input: N = 10

Output: 1 2 3 4 5 6 7 8 9 10

### Example 2:
Input:N = 5

Output: 1 2 3 4 5
 

### **Your Task:**
**This is a function problem. You only need to complete the function printNos() that takes N as parameter and prints number from 1 to N recursively. Don't print newline, it will be added by the driver code.**

Expected Time Complexity: O(N).

Expected Auxiliary Space: O(N) (Recursive).

Constraints: 1 <= N <= 1000 

```python
 #User function Template for python3

class Solution:    
    #Complete this function
    def printNos(self,N):
        #Your code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3

import math




def main():
    
    T=int(input())
    
    while(T>0):
        
        
        N=int(input())
        
        ob=Solution()
        
        ob.printNos(N)
        print()
        T-=1

if __name__=="__main__":
    main()
# } Driver Code Ends
```
</details>


<details>
<summary> Print Array Elements Using Recursion </summary>

      Dificulty Level : Basic
 You are given an array arr of size n. You need to print the array elements from start to end using given recursive function.


Example 1:

Input: n = 5
      
arr[] = {1,2,3,4,5}
      
Output: 1 2 3 4 5

Example 2:

Input: n = 4
      
arr[] = {5,4,2,1}
      
Output: 5 4 2 1
 

Your Task:
      
Complete the function printArrayRecursively() that takes array and size n as parameters and prints the array elements recursively. The newline is provided by driver code.

      
Expected Time Complexity: O(N).
Expected Auxiliary Space: O(N) (Recursive).
      
Constraints:
1 <= n <= 100
      
</details>

<details>
<summary> Sum of Digits of a Number  </summary>

      Dificulty Level : Basic
You are given a number n. You need to find the sum of digits of n.

Example 1:

Input:
n = 1
Output: 1
Explanation: Sum of digit of 1 is 1.
Example 2:

Input:
n = 99999
Output: 45
Explanation: Sum of digit of 99999 is 45.
Your Task:
You don't need to read input or print anything. Your task is to complete the function sumOfDigits() that takes n as parameter and returns the sum of digits of n.

Expected Time Complexity: O(Logn).
Expected Auxiliary Space: O(Logn) (Recursive).

Constraints:
1 <= n <= 107

```python
 #User function Template for python3

class Solution:
    def sumOfDigits(self, n):
        '''
        :param n: given number
        :return: sum of digits of n.
        '''
        # code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3
import atexit
import io
import sys

#Contributed by : Nagendra Jha

_INPUT_LINES = sys.stdin.read().splitlines()
input = iter(_INPUT_LINES).__next__
_OUTPUT_BUFFER = io.StringIO()
sys.stdout = _OUTPUT_BUFFER

@atexit.register

def write():
    sys.__stdout__.write(_OUTPUT_BUFFER.getvalue())

if __name__ == '__main__':
    test_cases = int(input())
    for cases in range(test_cases) :
        n = int(input())
        print(Solution().sumOfDigits(n))
# } Driver Code Ends

```
</details>

<details>
<summary>Count Total Digits in a Number</summary>
      
      Dificulty Level : Basic      
You are given a number n. You need to find the count of digits in n.

Example 1:

Input:
n = 1
Output: 1
Explanation: Number of digit in 1 is 1.
Example 2:

Input:
n  = 99999
Output: 5
Explanation:Number of digit in 99999 is 5
Your Task:
You don't need to read input or print anything. Your task is to complete the function countDigits() that takes n as parameter and returns the count of digits in n.

Expected Time Complexity: O(Logn).
Expected Auxiliary Space: O(Logn).

Constraints:
0 <= n <= 107 
      
```python    
#User function Template for python3

class Solution:
    def countDigits(self, n):
        '''
        :param n: given number
        :return: count of digits of n.
        '''
        # code here


#{ 
 # Driver Code Starts
#Initial Template for Python 3
import atexit
import io
import sys

#Contributed by : Nagendra Jha
_INPUT_LINES = sys.stdin.read().splitlines()
input = iter(_INPUT_LINES).__next__
_OUTPUT_BUFFER = io.StringIO()
sys.stdout = _OUTPUT_BUFFER

@atexit.register

def write():
    sys.__stdout__.write(_OUTPUT_BUFFER.getvalue())

if __name__ == '__main__':
    test_cases = int(input())
    for cases in range(test_cases) :
        n = int(input())
        print(Solution().countDigits(n))
# } Driver Code Ends
```
</details>
