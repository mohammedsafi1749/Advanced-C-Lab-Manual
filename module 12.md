

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
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp;
    temp=head;
    while(temp!=NULL){
        printf("%.3f\n",temp->data);
        temp=temp->next;
    }
}

Output:

//paste your output here
Test	Expected	Got	
head=NULL;
push(10.10);
push(11.11);
push(12.12);
display();
12.120
11.110
10.100
12.120
11.110
10.100
head=NULL;
push(101.11);
push(102.12);
push(103.13);
display();
103.130
102.120
101.110
103.130
102.120
101.110
head=NULL;
push(0.0);
display();
0.000
0.000


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

//type your code here
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()  
{ 
    if(head==NULL){
        printf("stack is empty");
    }
    else{
        head=head->next;
    }
}

Output:

//paste your output here
	Test	Expected	Got	
head=NULL;
push(10.01);
push(20.02);
push(30.03);
display();
pop();
printf("\nafter pop ");
display();
stack elements:30.03 20.02 10.01
after pop stack elements:20.02 10.01
stack elements:30.03 20.02 10.01
after pop stack elements:20.02 10.01
head=NULL;
push(101.01);
push(201.01);
push(301.01);
display();
pop();
printf("\nafter pop ");
display();
stack elements:301.01 201.01 101.01
after pop stack elements:201.01 101.01
stack elements:301.01 201.01 101.01
after pop stack elements:201.01 101.01
head=NULL;
pop();
stack is empty
stack is empty


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

//type your code here
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    if (front == NULL) {
        printf("queue is empty\n");
        return;
    }
    
    struct Node* temp = front;
    
    while (temp != NULL) {
        printf("%d\n", temp->data);
        temp = temp->next;
    }
    
}

Output:

//paste your output here
Test	Expected	Got	
front=NULL;
rear=NULL;
enqueue(5);
enqueue(10);
enqueue(15);
display();
5
10
15
5
10
15
front=NULL;
rear=NULL;
enqueue(100);
enqueue(200);
enqueue(300);
display();
100
200
300
100
200
300
front=NULL;
rear=NULL;
display();
queue is empty
queue is empty


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
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node *n=(struct Node*)malloc(sizeof(struct Node));
    n->data=data;
    n->next=NULL;
    if(front==NULL){
        front=rear=n;
    }
    else{
        rear->next=n;
        rear=n;
    }
}

Output:

//paste your output here
Test	Expected	Got	
front=NULL;
rear=NULL;
enqueue(1.1);
enqueue(2.2);
enqueue(3.3);
display();
queue elements:
1.100
2.200
3.300
queue elements:
1.100
2.200
3.300
front=NULL;
rear=NULL;
enqueue(100.11);
enqueue(200.11);
enqueue(300.11);
display();
queue elements:
100.110
200.110
300.110
queue elements:
100.110
200.110
300.110
front=NULL;
rear=NULL;
display();
queue is empty
queue is empty

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

//type your code here
struct Node{
    char data;
    struct Node*next;
    
}*head;
void peek(){
    if(head==NULL){
        printf("Stack underflow");
    }
    else{
        printf("%c",head->data);
    }
}

Output:

//paste your output here

Test	Expected	Got	
head=NULL;
push('A');
push('B');
push('C');
peek();
C
C
head=NULL;
push('a');
push('b');
push('c');
peek();
c
c


Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


