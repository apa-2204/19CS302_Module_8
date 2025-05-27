# # Task

# # Given a positive integer denoting , do the following:

# If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 41 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Input Format

The first line contains a single integer, .

## Constraints

## Output Format

If  41<=n <=49 print the lowercase English word corresponding to the number (e.g., forty one for 4 , forty two for 42 etc.).
If n>49 print Greater than 49.
## Sample Input

41
## Sample Output

forty one

## AIM: 
To write a program to print the sum and difference of the given two integers . 
 
 
## ALGORITHM: 
1. Start. 
2. Define a variables. 
3. Write a program to print the sum and difference of the integers.. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End. 
 
## PROGRAM: 
```
#include <stdio.h> 
 
int main() { 
    int a, b; 
    int sum, difference; 
 
    // Input two numbers 
    printf("Enter two 
integers: "); 
    scanf("%d %d", &a, 
&b); 
 
    // Calculate sum and 
difference 
    sum = a + b; 
    difference = a - b; 
 
    // Print the results 
    printf("Sum = 
%d\n", sum); 
    printf("Difference = 
%d\n", difference); 
 
    return 0; 
} 
 ```
 
## OUTPUT: 
 ![image](https://github.com/user-attachments/assets/75453ddf-d7ea-44c2-bf59-a52b949179a1)

 
## RESULT: 
Thus, the program is executed and verified successfully. 
