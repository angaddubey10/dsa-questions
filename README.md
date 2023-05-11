# Recursion Problems
## The Sequence 
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
