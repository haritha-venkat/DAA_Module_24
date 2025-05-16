# EX 6D BRUTE FORCE ALGORITHM
## DATE:

## AIM:
To write a python program using brute force method of searching for the given substring in the main string.

## Algorithm

1. Get lengths of `string` and `sub`.
2. Loop over each possible starting index `i` in `string` where `sub` could fit.
3. Slice `string[i:i+len(sub)]` and check if it equals `sub`.
4. If it matches, print the found index `i`.
5. Continue until all matches are found.

If you want, I can help you add the call to `match` function and test it with your inputs!
   

## Program:
```
/*
To implement the program using brute force method of searching for the given substring in the main string.


Developed by: haritha shree
Register Number:  212222230046
*/
def match(string,sub):
    l = len(string)
    ls = len(sub)
    start = sub[0]
    for i in range(l-ls+1):
        if string[i:i+ls]==sub:
            print(f"Found at index {i}")

str1=input()
str2=input()

```

## Output:

![Screenshot 2025-05-16 184748](https://github.com/user-attachments/assets/04503fdb-25a1-4ff5-b1b4-66939dab5c59)


## Result:
Thus the above program was executed successfully for searching the substring at respective index.
