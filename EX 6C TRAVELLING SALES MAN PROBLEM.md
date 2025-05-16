# EX 6C TRAVELLING SALES MAN PROBLEM
## DATE:
## AIM:
To Solve Travelling Sales man Problem for the following graph.

![image](https://github.com/user-attachments/assets/653921a4-3d7b-4691-9b41-735e80f7af0b)



## Algorithm

1. Generate all permutations of vertices excluding the start vertex `s`.
2. For each permutation, calculate the total path cost starting from `s`, visiting all vertices in order, and returning to `s`.
3. Keep track of the minimum path cost found among all permutations.
4. Use `itertools.permutations` to generate permutations efficiently.
5. Return the minimum path cost as the solution to the TSP.
 

## Program:
```
/*
To implement the program for TSP.


Developed by: haritha shree
Register Number:  212222230046
*/
from sys import maxsize
from itertools import permutations
V = 4
 

def travellingSalesmanProblem(graph, s):
    ##Write your code
    vertex = [] 
    for i in range(V): 
        if i != s: 
            vertex.append(i) 
    min_path = maxsize 
    next_permutation=permutations(vertex)
    for i in next_permutation:

        current_pathweight = 0
        k = s 
        for j in i: 
            current_pathweight += graph[k][j] 
            k = j 
        current_pathweight += graph[k][s] 
        min_path = min(min_path, current_pathweight) 
         
    return min_path
   
 
 

if __name__ == "__main__":
    graph = [[0, 10, 15, 20], [10, 0, 35, 25],
            [15, 35, 0, 30], [20, 25, 30, 0]]
    s = 0
    print(travellingSalesmanProblem(graph, s))
```

## Output:
![Screenshot 2025-05-16 184638](https://github.com/user-attachments/assets/cc782a29-9900-4e5a-8b93-c591b25cecfe)



## Result:
Thus the program was executed successfully for finding the minimum cost to vist all cities.
