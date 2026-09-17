EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top=-1;
void push(int item)
{
    if(top==MAX-1)
        printf("Stack Overflow\n");
    else
        stack[++top]=item;
}
void display()
{
    int i;
    if(top==-1)
        printf("Stack is Empty\n");
    else
    {
        printf("Stack elements are:\n");
        for(i=top;i>=0;i--)
            printf("%d\n",stack[i]);
    }
}
int main()
{
    push(10);
    push(20);
    push(30);
    push(40);
    display();
    return 0;
}
```

//type your code here

Output:

<img width="277" height="206" alt="image" src="https://github.com/user-attachments/assets/dc33df8c-6517-47bd-ab6b-6a23238f6c55" />

//paste your output here



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top=-1;

void push(int item)
{
    if(top==MAX-1)
        printf("Stack Overflow\n");
    else
    {
        top++;
        stack[top]=item;
        printf("%d pushed into stack\n",item);
    }
}

int main()
{
    int item;
    printf("Enter element to push: ");
    scanf("%d",&item);
    push(item);
    return 0;
}
```

//type your code here

Output:

<img width="316" height="147" alt="image" src="https://github.com/user-attachments/assets/2953779d-f008-4969-b849-3e6b306f30e7" />


//paste your output here




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
```
#include <stdio.h>
#define MAX 5

int queue[MAX]={10,20,30,40,50};
int front=0,rear=4;

void display()
{
    int i;
    if(front>rear)
        printf("Queue is Empty\n");
    else
    {
        printf("Queue elements are:\n");
        for(i=front;i<=rear;i++)
            printf("%d\n",queue[i]);
    }
}

int main()
{
    display();
    return 0;
}
```

//type your code here

Output:

<img width="307" height="222" alt="image" src="https://github.com/user-attachments/assets/c3008677-d894-4fe5-987a-266409ab701d" />

//paste your output here


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front=0,rear=-1;

void enqueue(int item)
{
    if(rear==MAX-1)
        printf("Queue Overflow\n");
    else
    {
        rear++;
        queue[rear]=item;
        printf("%d inserted into queue\n",item);
    }
}

int main()
{
    int item;
    printf("Enter element to insert: ");
    scanf("%d",&item);
    enqueue(item);
    return 0;
}
```

//type your code here

Output:

<img width="390" height="157" alt="image" src="https://github.com/user-attachments/assets/390d8f02-82a3-4ae7-b0c9-57273d33a615" />

//paste your output here

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
#include <stdio.h>
#define MAX 5

int queue[MAX]={10,20,30,40,50};
int front=0,rear=4;

void dequeue()
{
    if(front==-1)
        printf("Queue is Empty\n");
    else
    {
        printf("Deleted element = %d\n",queue[front]);
        front++;
        if(front>rear)
        {
            front=-1;
            rear=-1;
        }
    }
}

int main()
{
    dequeue();
    return 0;
}
```

//type your code here

Output:

<img width="317" height="137" alt="image" src="https://github.com/user-attachments/assets/fc824703-36c9-470c-8e36-63e28eea034e" />

//paste your output here


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
