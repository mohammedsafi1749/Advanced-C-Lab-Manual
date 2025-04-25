EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
#include<stdio.h>
struct intg
{
    int a;
    char b[20];
};
int main()
{
    struct intg s;
    scanf("%d",&s.a);
    scanf("%s",s.b);
    
   if(s.a>18)
   {
       printf("Age:%d\n",s.a);
       printf("Name:%svaccine:%d\n",s.b,s.a);
       printf("eligibility:yes");
   }
   else
   {
       printf("Age:%d\n",s.a);
       
       printf("Name:%s",s.b);
       printf("vaccine:%d\n",s.a);
       printf("eligibility:no");
   }
 return 0;
}


Output:
	Input	Expected	Got	
21
ramesh
Age:21
Name:rameshvaccine:21
eligibility:yes
Age:21
Name:rameshvaccine:21
eligibility:yes
18
shiva
Age:18
Name:shivavaccine:18
eligibility:no
Age:18
Name:shivavaccine:18
eligibility:no

Result:
Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:

#include <stdio.h>

struct num{
    int a;
    int b;
    int res;
}n;

int add(struct num n);

int main()
{
    scanf("%d %d",&n.a,&n.b);
    n.res = add(n);
    printf("%d",n.res);
}
int add(struct num n)
{
    int ans;
    ans = n.a + n.b;
    return ans;
}




Output:


	Input	Expected	Got	
10
20
30
30
50
-20
30
30
-20
-30
-50
-50


Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

#include <stdio.h>
int main()
{
   char name[50];
   scanf(" %s",name);
   FILE *fptr;
   fptr = (fopen("name","w"));
   if(fptr == NULL)
   {
       printf("Error!");
       //exit(1);
   }

   else
   {
      printf("%s File Created Successfully\n",name);
      printf("%s File Opened\n",name);
   }

   fclose(fptr);
   printf("%s File Closed\n",name);
   return 0;
}




Output:


//paste your output here
	Input	Expected	Got	
Employee.txt
Employee.txt File Created Successfully
Employee.txt File Opened
Employee.txt File Closed
Employee.txt File Created Successfully
Employee.txt File Opened
Employee.txt File Closed
Student.txt
Student.txt File Created Successfully
Student.txt File Opened
Student.txt File Closed
Student.txt File Created Successfully
Student.txt File Opened
Student.txt File Closed
Sample.c
Sample.c File Created Successfully
Sample.c File Opened
Sample.c File Closed
Sample.c File Created Successfully
Sample.c File Opened
Sample.c File Closed










Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

//type your code here
#include <stdio.h>
int main()
{
   char name[50];
   int i,num;
   float f;

   scanf("%s", name);
   scanf("%d", &num);
   
   FILE*fptr;
   fptr = (fopen(name, "w"));
   if(fptr == NULL)
   {
       printf("Error!");
       //exit(1);
   }
   //printf("%p Opened\n",fptr);
   printf("%s Opened\n",name);
   for(i = 0; i < num; ++i)
   {
      
      scanf("%f", &f);

      fprintf(fptr,"%f \n", f);
   }
   printf("Data added Successfully");
   fclose(fptr);
   return 0;
}



Output:


//paste your output here
Input	Expected	Got	
Sample.txt
2
aaa
bbb
Sample.txt Opened
Data added Successfully
Sample.txt Opened
Data added Successfully
Rawee.txt
3
RAWEE
KUMAR
CHARVIQ
Rawee.txt Opened
Data added Successfully
Rawee.txt Opened
Data added Successfully






Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

//type your code here
#include <stdio.h>

// Defining the structure
struct Student {
    int admission_no;
    char student_name[20];
    char course_type[40];
    char course_name[100];
    int tuition_fee;
    
    struct Date_of_admission {
        int dd;
        int mm;
        int yyyy;
    } doj;
};

int main() {
    struct Student e1;

    
    scanf("%d", &e1.admission_no);

   
    scanf("%s", e1.student_name);

   
    scanf("%s", e1.course_name);

   
    scanf("%s", e1.course_type);

   
    scanf("%d", &e1.tuition_fee);

   
    scanf("%d %d %d", &e1.doj.dd, &e1.doj.mm, &e1.doj.yyyy);

   
    printf("Admission Number : %d\n", e1.admission_no);
    printf("Student name : %s\n", e1.student_name);
    printf("Course Type : %s\n", e1.course_type);
    printf("Date of admission (dd/mm/yyyy) : %d/%d/%d\n", e1.doj.dd, e1.doj.mm, e1.doj.yyyy);
    printf("Course Name :%s\n", e1.course_name);
    printf("Tution Fee:%d\n", e1.tuition_fee);

    return 0;
}




Output:


//paste your output here

Input	Expected	Got	
120365
shanker
BE-CSE
undergraduate
50000
12
03
2021
Admission Number : 120365
Student name : shanker
Course Type : undergraduate
Date of admission (dd/mm/yyyy) : 12/3/2021
Course Name :BE-CSE
Tution Fee:50000
Admission Number : 120365
Student name : shanker
Course Type : undergraduate
Date of admission (dd/mm/yyyy) : 12/3/2021
Course Name :BE-CSE
Tution Fee:50000
145026
Reena
BE-ECE
Undergraduate
60000
15
09
2021
Admission Number : 145026
Student name : Reena
Course Type : Undergraduate
Date of admission (dd/mm/yyyy) : 15/9/2021
Course Name :BE-ECE
Tution Fee:60000
Admission Number : 145026
Student name : Reena
Course Type : Undergraduate
Date of admission (dd/mm/yyyy) : 15/9/2021
Course Name :BE-ECE
Tution Fee:60000




Result:
Thus, the program is verified successfully
