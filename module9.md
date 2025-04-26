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

//type your code here
char stack[100];
int top;
void display()
{
    
    int i;
    for(i=top;i>=0;i--)
    {
        printf("%c\n",stack[i]);
    }
}

Output:

//paste your output here
Test	Expected	Got	
top=-1;
push('A');
push('B');
push('C');
display();
C
B
A
C
B
A
top=-1;
push('a');
push('e');
push('i');
display();
i
e
a
i
e
a
top=-1;
push('X');
push('Y');
push('Z');
display();
Z
Y
X
Z
Y
X




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

//type your code here
float stack[100];
int size=3,top=-1;
void push (float data)
{
    stack[++top]=data;
}

Output:

//paste your output here
Test	Expected	Got	
top=-1;
push(10.5);
push(20.5);
push(30.5);
display();
30.5
20.5
10.5
30.5
20.5
10.5
top=-1;
push(100.1);
push(200.1);
push(300.1);
display();
300.1
200.1
100.1
300.1
200.1
100.1
top=-1;
push(5.5);
push(6.5);
push(7.5);
display();
7.5
6.5
5.5
7.5
6.5
5.5




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

//type your code here
float queue[50];
int front,rear;

void display()
{
    if(front==-1 || front>rear)
    {
        printf("No elements to display\n");
    }
    else
    {
        for(int i=front;i<=rear;i++)
        {
            printf("%.1f ",queue[i]);
        }
    }
}

Output:

//paste your output here
Test	Expected	Got	
rear=-1;
front=-1;
enqueue(100.5);
enqueue(200.5);
enqueue(300.5);
display();
100.5 200.5 300.5
100.5 200.5 300.5
rear=-1;
front=-1;
enqueue(1.1);
enqueue(2.2);
enqueue(3.3);
display();
1.1 2.2 3.3
1.1 2.2 3.3
rear=-1;
front=-1;
display();
No elements to display
No elements to display


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

//type your code here
char queue[50];
int front,rear;
int size=3;
void enqueue(char data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear+=1;
        queue[rear]=data;
    }
    
}


Output:

//paste your output here
Test	Expected	Got	
rear=-1; front=-1;
enqueue('A');
enqueue('B');
enqueue('C');
display();
A
B
C
A
B
C
rear=-1; front=-1;
enqueue('x');
enqueue('y');
enqueue('z');
display();
x
y
z
x
y
z
rear=-1; front=-1;
display();
no elements to display
no elements to display


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

//type your code here
int front,rear;
void dequeue()
{
    if(front==-1 || front>rear)
    {
        printf("c");
    }
    else
    {
        front++;
    }
}

Output:

//paste your output here
Test	Expected	Got	
enqueue(100);
enqueue(200);
enqueue(300);
display();
dequeue();
display();
100 200 300 200 300
100 200 300 200 300
rear=-1;
front=-1;
enqueue(5);
enqueue(50);
enqueue(500);
display();
dequeue();
display();
5 50 500 50 500
5 50 500 50 500
rear=-1;
front=-1;
enqueue(30);
display();
dequeue();
display();
30 No elements to display
30 No elements to display


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
