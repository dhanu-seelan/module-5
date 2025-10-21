# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

#include <stdio.h>

int main()
{
    float length, breadth, area;
    float *x, *y;

   
    printf("Enter length of the rectangle: ");
    scanf("%f", &length);
    printf("Enter breadth of the rectangle: ");
    scanf("%f", &breadth);

   
    x = &length;
    y = &breadth;


    area = (*x) * (*y);

    
    printf("Area of the rectangle = %.2f\n", area);

    
    return 0;
}


## OUTPUT
		       	
<img width="1786" height="960" alt="image" src="https://github.com/user-attachments/assets/84eaaccf-228a-447e-875f-021e4cb1a702" />


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM

#include <stdio.h>
#include <stdlib.h>

int main()
{
    char *str;

   
    str = (char *)malloc(8 * sizeof(char));  

    if (str == NULL)
    {
        printf("Memory not allocated.\n");
        return 1;
    }

  
    str = "WELCOME";

    printf("%s\n", str);


    return 0;
}


## OUTPUT
<img width="1781" height="964" alt="image" src="https://github.com/user-attachments/assets/a00f28a6-c271-4985-a75a-8ed2fbd2d287" />



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
#include <stdio.h>
struct student
{
    char name[50];
    int rollno;
    float marks;
};

int main()
{
    struct student s; 
    printf("Enter student name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.rollno);
    printf("Enter marks: ");
    scanf("%f", &s.marks);

   
    printf("\n--- Student Information ---\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.rollno);
    printf("Marks: %.2f\n", s.marks);

   
    return 0;
}


## OUTPUT
<img width="1864" height="966" alt="image" src="https://github.com/user-attachments/assets/a9466e7a-cdb6-4d56-8a53-416cb7e93599" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM

#include <stdio.h>


struct employee
{
    char name[50];
    int id;
    float basic, hra, da, gross;
};

int main()
{
    struct employee e[3]; 
    int i;

   
    for(i = 0; i < 3; i++)
    {
        printf("\nEnter details of Employee %d:\n", i + 1);
        printf("Enter Name: ");
        scanf("%s", e[i].name);
        printf("Enter ID: ");
        scanf("%d", &e[i].id);
        printf("Enter Basic Salary: ");
        scanf("%f", &e[i].basic);

        
        e[i].hra = 0.10 * e[i].basic;  
        e[i].da  = 0.05 * e[i].basic;  
        e[i].gross = e[i].basic + e[i].hra + e[i].da;
    }

    printf("\n--- Employee Details ---\n");
    for(i = 0; i < 3; i++)
    {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name: %s\n", e[i].name);
        printf("ID: %d\n", e[i].id);
        printf("Basic Salary: %.2f\n", e[i].basic);
        printf("HRA: %.2f\n", e[i].hra);
        printf("DA: %.2f\n", e[i].da);
        printf("Gross Salary: %.2f\n", e[i].gross);
    }

  
    return 0;
}

 ## OUTPUT
<img width="1901" height="891" alt="image" src="https://github.com/user-attachments/assets/a1243f4e-af1b-4bfb-8b98-afbadbd676a6" />
<img width="1887" height="963" alt="image" src="https://github.com/user-attachments/assets/b5de5aeb-9fad-475f-9a32-dfd24a6724c6" />
<img width="1806" height="964" alt="image" src="https://github.com/user-attachments/assets/bbd4a0da-1ea1-426d-a985-9d92af86e044" />

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
#include <stdio.h>

struct student{
    char name[10];
    int rollno;
    int subject[5];
    int total;
    float average;
};

int main()
{
    struct student s[2]; 
    int i, j;

   
    for(i = 0; i < 2; i++)
    {
        printf("\nEnter details of Student %d:\n", i + 1);

        printf("Enter name: ");
        scanf("%s", s[i].name);

        printf("Enter roll number: ");
        scanf("%d", &s[i].rollno);

        printf("Enter marks of 5 subjects:\n");
        for(j = 0; j < 5; j++)
        {
            printf("Subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
        }
    }

  
    for(i = 0; i < 2; i++)
    {
        s[i].total = 0;
        for(j = 0; j < 5; j++)
        {
            s[i].total += s[i].subject[j];
        }
        s[i].average = s[i].total / 5.0;
    }

   
    printf("\n--- Student Result ---\n");
    for(i = 0; i < 2; i++)
    {
        printf("\nStudent %d:\n", i + 1);
        printf("Name: %s\n", s[i].name);
        printf("Roll No: %d\n", s[i].rollno);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n", s[i].average);
    }


    return 0;
}


## OUTPUT
<img width="1825" height="965" alt="image" src="https://github.com/user-attachments/assets/c80897a1-0ff6-450f-b6f2-59a90cb5cd90" />
<img width="1865" height="968" alt="image" src="https://github.com/user-attachments/assets/1464f89c-223f-464b-8161-1e6188d6bad4" />


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


