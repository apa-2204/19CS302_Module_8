## Given an array of strings sorted in lexicographical order, print all of its permutations in strict lexicographical order. If two permutations look the same, only print one of them. See the 'note' below for an example.

Complete the function next_permutation which generates the permutations in the described order.

## For example, s=[ab,bc,cd]. The six permutations in correct order are:

ab bc cd
ab cd bc
bc ab cd
bc cd ab
cd ab bc
cd bc ab
Note: There may be two or more of the same string as elements of .
## For example, s=[ab,bc,cd]. Only one instance of a permutation where all elements match should be printed. In other words, if s[0]==s[1], then print either s[0]  or s[1] but not both.

A three element array having three distinct elements has six permutations as shown above. In this case, there are three matching pairs of permutations where ab and ba are switched. We only print the three visibly unique permutations:

ab ab bc
ab bc ab
bc ab ab
## Input Format

The first line of each test file contains a single integer , the length of the string array .

Each of the next  lines contains a string .

Constraints

 contains only lowercase English letters.
Output Format

Print each permutation as a list of space-separated strings on a single line.

## Sample Input 0

2
ab
cd
## Sample Output 0

ab cd
cd ab
## Sample Input 1

3
a
bc
bc
## Sample Output 1

a bc bc
bc a bc
bc bc a


## AIM:
To write a C program to generate and print all unique permutations of a string array in strict lexicographical order.

## ALGORITHM:
1.Start the program.
2.Read the number of strings n.
3.Read the array of strings.
4.Sort the array in lexicographical order.
5.Use a custom next_permutation() function to generate the next lexicographically greater permutation.
6.Print the current permutation.
7.Repeat until no further permutations exist.
8.End the program.

## PROGRAM:
```

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <stdbool.h>

int compare(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}

bool next_permutation(char *arr[], int n) {
    int i = n - 2;
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0)
        i--;
    if (i < 0) return false;

    int j = n - 1;
    while (strcmp(arr[i], arr[j]) >= 0)
        j--;

    // Swap arr[i] and arr[j]
    char *temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;

    // Reverse arr[i+1] to arr[n-1]
    int left = i + 1, right = n - 1;
    while (left < right) {
        temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;
        left++;
        right--;
    }
    return true;
}

void print_permutation(char *arr[], int n) {
    for (int i = 0; i < n; i++) {
        printf("%s ", arr[i]);
    }
    printf("\n");
}

int main() {
    int n;
    scanf("%d", &n);

    char *arr[100];
    for (int i = 0; i < n; i++) {
        arr[i] = malloc(100);
        scanf("%s", arr[i]);
    }

    // Sort array to start from the smallest lexicographical permutation
    qsort(arr, n, sizeof(char *), compare);

    // Print all unique permutations
    print_permutation(arr, n);
    while (next_permutation(arr, n)) {
        print_permutation(arr, n);
    }

    // Free memory
    for (int i = 0; i < n; i++) {
        free(arr[i]);
    }

    return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/5555a9bc-9e61-4b2f-bf77-806d9bca74e4)

## RESULT:

The C program was successfully compiled and executed. It printed all unique permutations of the input strings in strict lexicographical order.
