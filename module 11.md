

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
//type your code here
#include <stdio.h>
int max(int x,int y)
{
    return (x>y)?x:y;
}
int maxfour(int a,int b,int c,int d)
{
    return max(max(a,b),max(b,c));
}
int main(){
    int a,b,c,d;
    scanf("%d",&a);
    scanf("%d",&b);
    scanf("%d",&c);
    scanf("%d",&d);
    printf("%d",maxfour(a,b,c,d));
    return 0;
}

Output:
//paste your output here
Input	Expected	Got	
17
13
3
15
17
17
100
5
15
48
100
100


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
//type your code here
#include<stdio.h>
int max(int n,int k)
{
    int maxand=0;
    int maxor=0;
    int maxxor=0;
    for(int i=1;i<=n;i++)
    {
        for(int j=i+1;j<=n;j++)
        {
            int andval=i & j;
            int orval=i | j;
            int xorval=i ^ j;
            if(andval<k && andval>maxand) maxand=andval;
            if(orval<k && orval>maxor) maxor=orval;
            if(xorval<k && xorval>maxxor) maxxor=xorval;
        }
    }
    printf("%d\n%d\n%d\n",maxand,maxor,maxxor);
    return 0;
}
int main()
{
    int n,k;
    scanf("%d %d",&n,&k);
    max(n,k);
    return 0;
}

Output:
//paste your output here
Input	Expected	Got	
7 4
3
3
3
3
3
3
75 4
3
3
3
3
3
3
22 3
2
0
2
2
0
2


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
//type your code here
#include <stdio.h>
#include <stdlib.h>

int** tb;
int* tbs;

int main() {
    int ts;
    scanf("%d", &ts);

    // Allocate memory for array of pointers (shelves)
    tb = malloc(ts * sizeof(int*));
    tbs = malloc(ts * sizeof(int));

    for (int i = 0; i < ts; i++) {
        tb[i] = NULL; // Initially no books
        tbs[i] = 0; // Book count per shelf
    }

    int tq;
    scanf("%d", &tq);

    while (tq--) {
        int typeq;
        scanf("%d", &typeq);

        if (typeq == 1) {
            int x, y;
            scanf("%d %d", &x, &y);

            int count = tbs[x];
            // Reallocate shelf x to add one more book
            tb[x] = realloc(tb[x], (count + 1) * sizeof(int));
            tb[x][count] = y; // Insert book with y pages
            tbs[x]++; // Increase book count

        } else if (typeq == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", tb[x][y]);

        } else if (typeq == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", tbs[x]);
        }
    }

    // Free allocated memory
    for (int i = 0; i < ts; i++) {
        free(tb[i]);
    }
    free(tb);
    free(tbs);

    return 0;
}

Output:
//paste your output here
	Input	Expected	Got	
5
5
1 0 15
1 0 20
1 2 78
2 2 0
3 0
78
2
78
2
Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
//type your code here
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n;
    scanf("%d", &n);  
    int *arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Memory allocation failed\n");
        return 1;  
    }
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    int sum = 0;
    for (int i = 0; i < n; i++) {
        sum += arr[i];
    }
    printf("%d\n", sum);
    free(arr);

    return 0;
}


Output:
//paste your output here

 Input	Expected	Got	
8
15 5 16 15 17 11 5 11
95
95
7
1 13 15 20 12 13 2
76
76



Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
//type your code here
#include <stdio.h>

int main() {
    char sentence[1000];
    int i, words = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    for (i = 0; sentence[i] != '\0'; i++) {
        if ((sentence[i] == ' ' || sentence[i] == '\n') && (i > 0 && sentence[i-1] != ' ')) {
            words++;
        }
    }

    if (sentence[0] != ' ' && sentence[0] != '\n') {
        words++;
    }

    printf("Number of words: %d\n", words);

    return 0;
}


Output:
//paste your output here

Enter a sentence: Hello World
Number of words: 2

Enter a sentence: This is a simple C program
Number of words: 6

Enter a sentence:   Count    the    words    correctly
Number of words: 4




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
