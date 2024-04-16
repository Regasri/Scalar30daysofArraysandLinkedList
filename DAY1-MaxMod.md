Problem Description
Given an array A of size N, Groot wants you to pick 2 indices i and j such that

1 <= i, j <= N
A[i] % A[j] is maximum among all possible pairs of (i, j).
Help Groot in finding the maximum value of A[i] % A[j] for some i, j.



Problem Constraints
1 <= N <= 100000
0 <= A[i] <= 100000



Input Format
First and only argument in an integer array A.



Output Format
Return an integer denoting the maximum value of A[i] % A[j] for any valid i, j.



Example Input
Input 1:
```
 A = [1, 2, 44, 3]
```
Input 2:
````
 A = [2, 6, 4]

````
Example Output
Output 1:
````
 3
````
Output 2:

 4


Example Explanation
Explanation 1:

 For i = 4, j = 3  A[i] % A[j] = 3 % 44 = 3.
 No pair exists which has more value than 3.
Explanation 2:

 For i = 3, j = 2  A[i] % A[j] = 4 % 6 = 4.
 
  ```
int Solution::solve(vector<int> &A) {
      sort(A.begin(),A.end());
      int n=A.size();
      int ans;
      for(int i=n-1;i>=0;i--){
          if(A[i-1]%A[i]!=0){
              ans=A[i-1];
              break;
          }
      }
      return ans;
  }
   

