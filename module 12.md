EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

//type your code here
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *head=NULL;

void push(int value)
{
    struct Node *newNode;
    newNode=(struct Node*)malloc(sizeof(struct Node));
    newNode->data=value;
    newNode->next=head;
    head=newNode;
}

void display()
{
    struct Node *p=head;
    if(p==NULL)
    {
        printf("Stack is Empty");
        return;
    }
    printf("Stack elements are:\n");
    while(p!=NULL)
    {
        printf("%d\n",p->data);
        p=p->next;
    }
}

int main()
{
    push(10);
    push(20);
    push(30);
    display();
    return 0;
}
```

Output:

//paste your output here

<img width="270" height="185" alt="image" src="https://github.com/user-attachments/assets/da7366f4-2c5b-48e9-ae4a-9403fbd6174d" />


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *head=NULL;

void push(int value)
{
    struct Node *newNode;
    newNode=(struct Node*)malloc(sizeof(struct Node));
    newNode->data=value;
    newNode->next=head;
    head=newNode;
}

void pop()
{
    struct Node *temp;
    if(head==NULL)
    {
        printf("Stack is empty");
        return;
    }
    temp=head;
    printf("Popped element = %d\n",head->data);
    head=head->next;
    free(temp);
}

int main()
{
    push(10);
    push(20);
    push(30);
    pop();
    return 0;
}
```
//type your code here

Output:


<img width="305" height="186" alt="image" src="https://github.com/user-attachments/assets/beaa652b-c33e-4a2e-8cf1-673e418d5637" />


//paste your output here



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front=NULL,*rear=NULL;

void enqueue(int value)
{
    struct Node *newNode;
    newNode=(struct Node*)malloc(sizeof(struct Node));
    newNode->data=value;
    newNode->next=NULL;
    if(rear==NULL)
    {
        front=rear=newNode;
        return;
    }
    rear->next=newNode;
    rear=newNode;
}

void display()
{
    struct Node *temp=front;
    if(front==NULL)
    {
        printf("Queue is Empty");
        return;
    }
    printf("Queue elements are:\n");
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    return 0;
}
```

//type your code here

Output:

//paste your output here

<img width="307" height="196" alt="image" src="https://github.com/user-attachments/assets/9b0f8d7b-a0aa-4832-8081-903d88121af8" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

//type your code here
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front=NULL,*rear=NULL;

void enqueue(int value)
{
    struct Node *p;
    p=(struct Node*)malloc(sizeof(struct Node));
    p->data=value;
    p->next=NULL;
    if(front==NULL)
    {
        front=rear=p;
    }
    else
    {
        rear->next=p;
        rear=p;
    }
    printf("%d inserted into queue\n",value);
}

int main()
{
    int value;
    printf("Enter element: ");
    scanf("%d",&value);
    enqueue(value);
    return 0;
}
```

Output:

//paste your output here


<img width="342" height="163" alt="image" src="https://github.com/user-attachments/assets/13961ee4-e2d6-4c18-8990-756b531b2a4d" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node *next;
};

struct Node *front=NULL,*rear=NULL;

void enqueue(int value)
{
    struct Node *p;
    p=(struct Node*)malloc(sizeof(struct Node));
    p->data=value;
    p->next=NULL;
    if(front==NULL)
        front=rear=p;
    else
    {
        rear->next=p;
        rear=p;
    }
}

void peek()
{
    if(front==NULL)
        printf("Queue is Empty");
    else
        printf("Front element = %d",front->data);
}

int main()
{
    enqueue(10);
    enqueue(20);
    enqueue(30);
    peek();
    return 0;
}
```
//type your code here

Output:

<img width="253" height="110" alt="image" src="https://github.com/user-attachments/assets/099bcd49-5f00-4a5d-bb35-6a4049fba67d" />

//paste your output here



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


