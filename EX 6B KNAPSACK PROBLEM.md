# EX 6B KNAPSACK PROBLEM
## DATE:

## AIM:
To demonstrate a python program using dynamic programming for 0/1 knapsack problem.


## Algorithm

1. Create a 2D DP table `K` of size `(n+1) x (W+1)` initialized with zeros.
2. Iterate over items (`i` from 0 to n) and capacities (`w` from 0 to W).
3. If no items or capacity zero, set `K[i][w] = 0`.
4. If current item weight `wt[i-1]` ≤ `w`, update `K[i][w] = max(val[i-1] + K[i-1][w-wt[i-1]], K[i-1][w])`.
5. Else copy the value from above row `K[i][w] = K[i-1][w]`. Return `K[n][W]` as max value.
 

## Program:
```
/*
To implement the program for 0/1 knapsack problem.


Developed by: 
Register Number:  
*/
def knapSack(W, wt, val, n):
    ########## Add your code here #########
    K = [[0 for x in range(W + 1)] for x in range(n + 1)]
    for i in range(n + 1):
        for w in range(W + 1):
            if i == 0 or w == 0:
                K[i][w] = 0
            elif wt[i-1] <= w:
                K[i][w] = max(val[i-1]+ K[i-1][w-wt[i-1]],K[i-1][w])
            else:
                K[i][w] = K[i-1][w]
 
    return K[n][W]

x=int(input())
y=int(input())
W=int(input())
val=[]
wt=[]
for i in range(x):
    val.append(int(input()))
for y in range(y):
    wt.append(int(input()))

n = len(val)
print('The maximum value that can be put in a knapsack of capacity W is: ',knapSack(W, wt, val, n))
```

## Output:
![Screenshot 2025-05-16 184459](https://github.com/user-attachments/assets/0bb8aaa2-3427-4596-aaa0-5fd2ec5f8df0)



## Result:
Thus the program was executed successfully for finding the maximum value that can be put in a knap sack of capacity .
