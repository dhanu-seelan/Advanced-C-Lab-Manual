

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

int max_of_four(int a,int b,int c,int d)
{
    if(a>=b&&a>=c&&a>=d)
        return a;
    else if(b>=a&&b>=c&&b>=d)
        return b;
    else if(c>=a&&c>=b&&c>=d)
        return c;
    else
        return d;
}

int main()
{
    int n1,n2,n3,n4,greater;
    printf("Enter four numbers: ");
    scanf("%d%d%d%d",&n1,&n2,&n3,&n4);
    greater=max_of_four(n1,n2,n3,n4);
    printf("Greatest number = %d",greater);
    return 0;
}
```
//type your code here

Output:

<img width="340" height="132" alt="image" src="https://github.com/user-attachments/assets/96b16b0e-a93e-4ac7-bfca-470e12192d8f" />

//paste your output here

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

void calculate_the_max(int n,int k)
{
    int i,j,a=0,o=0,x=0;
    for(i=1;i<=n;i++)
    {
        for(j=i+1;j<=n;j++)
        {
            if((i&j)<k&&(i&j)>a)
                a=i&j;
            if((i|j)<k&&(i|j)>o)
                o=i|j;
            if((i^j)<k&&(i^j)>x)
                x=i^j;
        }
    }
    printf("%d\n",a);
    printf("%d\n",o);
    printf("%d\n",x);
}

int main()
{
    int n,k;
    printf("Enter n and k: ");
    scanf("%d%d",&n,&k);
    calculate_the_max(n,k);
    return 0;
}
```
//type your code here

Output:

<img width="316" height="167" alt="image" src="https://github.com/user-attachments/assets/6a67a9ad-333a-4440-b67c-a38050cc26f1" />

//paste your output here

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
#include <stdlib.h>

int main()
{
    int noshel,noque;
    scanf("%d%d",&noshel,&noque);
    int **shelarr=(int **)malloc(noshel*sizeof(int *));
    int *nobookarr=(int *)calloc(noshel,sizeof(int));
    int type,x,y;
    while(noque--)
    {
        scanf("%d",&type);
        if(type==1)
        {
            scanf("%d%d",&x,&y);
            nobookarr[x]++;
            shelarr[x]=(int *)realloc(shelarr[x],nobookarr[x]*sizeof(int));
            shelarr[x][nobookarr[x]-1]=y;
        }
        else if(type==2)
        {
            scanf("%d%d",&x,&y);
            printf("%d\n",shelarr[x][y]);
        }
        else if(type==3)
        {
            scanf("%d",&x);
            printf("%d\n",nobookarr[x]);
        }
    }
    for(int i=0;i<noshel;i++)
        free(shelarr[i]);
    free(shelarr);
    free(nobookarr);
    return 0;
}
```
//type your code here

Output:

```
2 5
1 0 10
1 0 20
3 0
2 0 1
3 1

2
20
0
```
//paste your output here


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
    int n,i,sum=0;
    printf("Enter number of elements: ");
    scanf("%d",&n);
    int a[n];
    printf("Enter the elements: ");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
        sum=sum+a[i];
    }
    printf("Sum = %d",sum);
    return 0;
}
```
//type your code here

Output:

<img width="342" height="117" alt="image" src="https://github.com/user-attachments/assets/f34e3f14-c799-47d1-b65c-16491b8e262e" />

//paste your output here

 


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
#include <string.h>

int main()
{
    char str[200];
    int i,count=0;
    printf("Enter a sentence: ");
    fgets(str,sizeof(str),stdin);
    for(i=0;str[i]!='\0';i++)
    {
        if((i==0&&str[i]!=' ')||(str[i]!=' '&&str[i-1]==' '))
            count++;
    }
    printf("Number of words = %d",count);
    return 0;
}
```
//type your code here

Output:
//paste your output here

<img width="355" height="117" alt="image" src="https://github.com/user-attachments/assets/542a2177-57b0-4cff-b38f-57915ec19773" />




Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
