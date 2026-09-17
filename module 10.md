EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

void search(struct node *head,int key)
{
    while(head!=NULL)
    {
        if(head->data==key)
        {
            printf("Element found");
            return;
        }
        head=head->next;
    }
    printf("Element not found");
}

int main()
{
    struct node *head,*second,*third;
    int key;
    head=(struct node*)malloc(sizeof(struct node));
    second=(struct node*)malloc(sizeof(struct node));
    third=(struct node*)malloc(sizeof(struct node));
    head->data=10;
    head->next=second;
    second->data=20;
    second->next=third;
    third->data=30;
    third->next=NULL;
    printf("Enter element to search: ");
    scanf("%d",&key);
    search(head,key);
    free(head);
    free(second);
    free(third);
    return 0;
}
```
//type your code here

Output:

<img width="357" height="140" alt="image" src="https://github.com/user-attachments/assets/06252904-56c4-4628-aedd-c7d79defab8c" />


//paste your output here



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *head=NULL;

void insert(int value)
{
    struct node *newnode,*temp;
    newnode=(struct node*)malloc(sizeof(struct node));
    newnode->data=value;
    newnode->next=NULL;
    if(head==NULL)
        head=newnode;
    else
    {
        temp=head;
        while(temp->next!=NULL)
            temp=temp->next;
        temp->next=newnode;
    }
}

void display()
{
    struct node *temp=head;
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
}

int main()
{
    int value;
    printf("Enter element to insert: ");
    scanf("%d",&value);
    insert(value);
    printf("Linked List: ");
    display();
    return 0;
}
```
//type your code here

Output:

<img width="363" height="141" alt="image" src="https://github.com/user-attachments/assets/8e9cafda-f4d1-47eb-80f2-a04096cc4d0f" />


//paste your output here

 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *prev;
    struct node *next;
};

int main()
{
    struct node *head,*second,*third,*temp;
    head=(struct node*)malloc(sizeof(struct node));
    second=(struct node*)malloc(sizeof(struct node));
    third=(struct node*)malloc(sizeof(struct node));

    head->data=10;
    head->prev=NULL;
    head->next=second;

    second->data=20;
    second->prev=head;
    second->next=third;

    third->data=30;
    third->prev=second;
    third->next=NULL;

    temp=head;

    printf("Doubly Linked List:\n");

    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }

    free(head);
    free(second);
    free(third);

    return 0;
}
```
//type your code here

Output:

<img width="303" height="138" alt="image" src="https://github.com/user-attachments/assets/5256a2ed-8d2b-4218-8823-01fd1f2bd63a" />


//paste your output here


Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *prev;
    struct node *next;
};

struct node *head=NULL;

void insert(int value)
{
    struct node *newNode,*temp;
    newNode=(struct node*)malloc(sizeof(struct node));
    newNode->data=value;
    newNode->next=NULL;
    newNode->prev=NULL;
    if(head==NULL)
        head=newNode;
    else
    {
        temp=head;
        while(temp->next!=NULL)
            temp=temp->next;
        temp->next=newNode;
        newNode->prev=temp;
    }
}

void display()
{
    struct node *temp=head;
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
}

int main()
{
    int value;
    printf("Enter element: ");
    scanf("%d",&value);
    insert(value);
    printf("Doubly Linked List: ");
    display();
    return 0;
}
```

//type your code here

Output:

<img width="303" height="138" alt="Screenshot 2026-09-17 110414" src="https://github.com/user-attachments/assets/bb028a40-3592-4235-aead-2bd8863a97b3" />


//paste your output here


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:

```
#include <stdio.h>
#include <stdlib.h>

struct node
{
    int data;
    struct node *next;
};

struct node *head=NULL;

void insert(int value)
{
    struct node *newnode,*temp;
    newnode=(struct node*)malloc(sizeof(struct node));
    newnode->data=value;
    newnode->next=NULL;
    if(head==NULL)
        head=newnode;
    else
    {
        temp=head;
        while(temp->next!=NULL)
            temp=temp->next;
        temp->next=newnode;
    }
}

void deleteNode(int key)
{
    struct node *temp=head,*prev=NULL;
    if(head==NULL)
    {
        printf("List is empty");
        return;
    }
    if(head->data==key)
    {
        temp=head;
        head=head->next;
        free(temp);
        return;
    }
    while(temp!=NULL&&temp->data!=key)
    {
        prev=temp;
        temp=temp->next;
    }
    if(temp==NULL)
    {
        printf("Element not found");
        return;
    }
    prev->next=temp->next;
    free(temp);
}

void display()
{
    struct node *temp=head;
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
}

int main()
{
    int key;
    insert(10);
    insert(20);
    insert(30);
    printf("Enter element to delete: ");
    scanf("%d",&key);
    deleteNode(key);
    printf("Linked List: ");
    display();
    return 0;
}
```
//type your code here

Output:

<img width="412" height="142" alt="image" src="https://github.com/user-attachments/assets/5520b1fe-ceed-4692-80bf-ac1d030192d2" />


//paste your output here





Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





