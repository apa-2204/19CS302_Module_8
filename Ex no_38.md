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
To write a program to print the English word corresponding to the given number. 
 
 
## ALGORITHM: 
1. Start. 
2. Define a variables. 
3. Write a program to print the English word corresponding to the given number. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End. 
 
## PROGRAM: 
```
#include <stdio.h> 
 
int main() { 
    int num; 
 
    printf("Enter a 
number (0-9): "); 
    scanf("%d", &num); 
 
    switch (num) { 
        case 0: 
printf("Zero\n"); break; 
        case 1: 
printf("One\n"); break; 
        case 2: 
printf("Two\n"); break; 
        case 3: 
printf("Three\n"); 
break; 
        case 4: 
printf("Four\n"); break; 
        case 5: 
printf("Five\n"); break; 
        case 6: 
printf("Six\n"); break; 
        case 7: 
printf("Seven\n"); 
break; 
        case 8: 
 SAVEETHA ENGINEERING COLLEGE  
printf("Eight\n"); 
break; 
        case 9: 
printf("Nine\n"); break; 
        default: 
printf("Invalid 
number!\n"); break; 
    } 
 
    return 0; 
} 
 ```
 
## OUTPUT: 
![image](https://github.com/user-attachments/assets/bd7d32c1-d8de-4542-a488-07de3d49047b)

 
## RESULT: 
Thus, the program is executed and verified successfully.
