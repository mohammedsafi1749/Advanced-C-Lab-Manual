EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

//type your code here
struct Node{
    char data; 
    struct Node *next;
};
struct Node *head;
void search(char data)
{
    struct Node *temp;
    int i=0,flag=0;
    temp=head;
    if(temp==NULL)
    {
        printf("Empty list\n");
    }
    else
    {
        while(temp!=NULL)
        {
            i++;
            if(temp->data==data)
            {
                flag=1;
                break;
            }
            temp=temp->next;
        }
        if(flag==1)
        {
            printf("item %c found at location %d\n",data,i);
        }
        else
        {
            printf("Item not found\n");
        }
    }
}

Output:

//paste your output here
Test	Expected	Got	
head = NULL;
insert('a');
insert('b');
insert('c');
search('a');
item a found at location 1
item a found at location 1
head = NULL;
insert('X');
insert('Y');
insert('Z');
search('Z');
item Z found at location 3
item Z found at location 3
head = NULL;
insert('A');
insert('B');
search('F');
Item not found
Item not found


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

//type your code here
struct Node{
    char  data; 
    struct Node *next;
}*head;
void insert(char data)
{
    struct Node *x=(struct Node *)malloc(sizeof(struct Node));
    struct Node *t=head;
    x->data=data;
    x->next=NULL;
    if(t==NULL)
    {
        head=x;
        return;
    }
    else
    {
        while(t->next!=NULL)
        {
            t=t->next;
        }
        t->next=x;
    }
}

Output:

//paste your output here
Test	Expected	Got	
head = NULL;
insert('A');
insert('B');
insert('C');
display();
A B C
A B C
head = NULL;
insert('x');
insert('y');
insert('z');
display();
x y z
x y z
head = NULL;
insert('@');
insert('#');
insert('$');
display();
@ # $
@ # $

 
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

//type your code here
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    struct Node *ptr;
    ptr = head;
    while(ptr!=NULL){
        printf("%.2f\n",ptr->data);
        ptr=ptr->next;
    }
}

Output:

//paste your output here
Test	Expected	Got	
head = NULL;
insert(10.1);
insert(20.2);
insert(30.3);
display();
10.10
20.20
30.30
10.10
20.20
30.30
head = NULL;
insert(100.5);
insert(200.5);
insert(300.5);
display();
100.50
200.50
300.50
100.50
200.50
300.50
head = NULL;
insert(0);
insert(50.55);
display();
0.00
50.55
0.00
50.55


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

//type your code here
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
};
struct Node *head;
void insert(int data)
{
    struct Node *temp;
    struct Node *newnode;
    temp=head;
    newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    if(head==0)
    {
        newnode->prev=0;
        newnode->next=0;
        head=newnode;
    }
    else
    {
        temp=head;
        while(temp->next!=0)
        {
            temp=temp->next;
        }
        temp->next=newnode;
        newnode->prev=temp;
        newnode->next=0;
    }
}

Output:

//paste your output here
Test	Expected	Got	
head = NULL;
insert(10);
insert(20);
insert(30);
display();
10
20
30
10
20
30
head = NULL;
insert(100);
insert(200);
insert(300);
display();
100
200
300
100
200
300
head = NULL;
insert(5);
display();
5
5


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

//type your code here
struct Node{
    int data; 
    struct Node *next;
}*head;
void delete()
{
    if(head==NULL)
    {
        printf("List is empty");
        return;
    }
    printf("Node deleted from the begining ...\n");
    struct Node *temp=head;
    head=head->next;
    
    free(temp);
    
    
}

Output:

//paste your output here
Test	Expected	Got	
head = NULL;
insert('a');
insert('b');
insert('c');
display();
delete();
display();
a b c Node deleted from the begining ...
b c
a b c Node deleted from the begining ...
b c
head = NULL;
insert('X');
insert('Y');
insert('Z');
display();
delete();
display();
X Y Z Node deleted from the begining ...
Y Z
X Y Z Node deleted from the begining ...
Y Z
head = NULL;
insert('g');
display();
delete();
display();
delete();
display();
g Node deleted from the begining ...
List is empty
g Node deleted from the begining ...
List is empty




Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





