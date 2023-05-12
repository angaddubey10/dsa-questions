# **Recursion Problems**
## **The Sequence**
      Dificulty Level : Basic
You are given a number n. You need to recursively find the nth term of the series S that is given by:
S(n) = n+ n*(S(n-1)) and S(0) = 1

Example 1:

  Input: n = 2

  Output: 6

Example 2:

  Input:
  n = 3

  Output: 21
  Your Task:

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

## **Print 1 To N Without Loop**
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

