

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
```
#include <stdio.h>

int greatest(int a, int b, int c)
{
    int max = a;

    if(b > max)
        max = b;

    if(c > max)
        max = c;

    return max;
}

int main()
{
    int a, b, c, result;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    result = greatest(a, b, c);

    printf("Greatest number = %d", result);

    return 0;
}
```

Output:
<img width="778" height="285" alt="image" src="https://github.com/user-attachments/assets/78863d40-55f9-456d-a079-9d54ac865d1c" />

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
```
#include <stdio.h>

int main()
{
    int n, k, i, j;
    int and_val, or_val, xor_val;
    int max_and = 0, max_or = 0, max_xor = 0;

    scanf("%d %d", &n, &k);

    for(i = 1; i <= n; i++)
    {
        for(j = i + 1; j <= n; j++)
        {
            and_val = i & j;
            or_val = i | j;
            xor_val = i ^ j;

            if(and_val > max_and && and_val < k)
                max_and = and_val;

            if(or_val > max_or && or_val < k)
                max_or = or_val;

            if(xor_val > max_xor && xor_val < k)
                max_xor = xor_val;
        }
    }

    printf("%d\n", max_and);
    printf("%d\n", max_or);
    printf("%d\n", max_xor);

    return 0;
}
```
Output:
<img width="775" height="276" alt="image" src="https://github.com/user-attachments/assets/5c3836d4-b745-4979-9d51-76852f31e67b" />


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
```
#include <stdio.h>

int main()
{
    int n, k, i, j;
    int and_val, or_val, xor_val;
    int max_and = 0, max_or = 0, max_xor = 0;

    scanf("%d %d", &n, &k);

    for(i = 1; i <= n; i++)
    {
        for(j = i + 1; j <= n; j++)
        {
            and_val = i & j;
            or_val = i | j;
            xor_val = i ^ j;

            if(and_val < k && and_val > max_and)
                max_and = and_val;

            if(or_val < k && or_val > max_or)
                max_or = or_val;

            if(xor_val < k && xor_val > max_xor)
                max_xor = xor_val;
        }
    }

    printf("%d\n", max_and);
    printf("%d\n", max_or);
    printf("%d\n", max_xor);

    return 0;
}
```

Output:
<img width="580" height="337" alt="image" src="https://github.com/user-attachments/assets/1a985602-6ee4-457b-896a-a85f870a2415" />



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
```
#include <stdio.h>

int main()
{
    int a[100], n, i, sum = 0;

    scanf("%d", &n);

    for(i = 0; i < n; i++)
    {
        scanf("%d", &a[i]);
        sum = sum + a[i];
    }

    printf("%d", sum);

    return 0;
}
```

Output:
<img width="856" height="367" alt="image" src="https://github.com/user-attachments/assets/c32a7e3f-29df-49c2-95d3-b43719e8e182" />


 


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
```
#include <stdio.h>

int main()
{
    char str[200];
    int i, count = 0;

    fgets(str, sizeof(str), stdin);

    for(i = 0; str[i] != '\0'; i++)
    {
        if(str[i] == ' ' && str[i + 1] != ' ')
            count++;
    }

    if(str[0] != '\n')
        count++;

    printf("%d", count);

    return 0;
}
```

Output:
<img width="852" height="397" alt="image" src="https://github.com/user-attachments/assets/17d76506-61c3-4d3a-bbee-ac52e7e5c468" />




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
