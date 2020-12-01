---
title: Structure and Union
date: "2020-10-20T23:46:37.121Z"
description: "Structure and Union"
---

### Structures

Structure is user defined data type that allows us to hold different kinds of data items. It is a collection of logically related variables referenced under one name.
Structures are used to represent a record.

Syntax:

```c
struct structure_name
{
    data_type member1;
    data_type member2;
    .
    .
    data_type memeberN;
};
```

```c
#include<stdio.h>
#include<string.h>
struct Employee
{   int id;
    char name[25];
}emp;  //declaring emp variable for structure
int main( )
{
   //stores employee information
   emp.id=1001;
   strcpy(emp.name, "Jazz Jenkins");
   //prints first employee information
   printf( "Employee id : %d\n", emp.id);
   printf( "Employee name : %s", emp.name);
return 0;
}
```

Output

```
Employee id : 1001
Employee name : Jazz Jenkins
```

#### Structure within structure

Structure within structure is also known as nesting of structure because a structure declaration is placed inside another structure. It is used to create complex records.

```c
struct Employee
{
	struct Man
	{
		char name [20];
		int age;
		int sal;
	} d;
int empid;
char desg[10];
} emp;
```

#### Array of structures

```c
#include<stdio.h>
#include <string.h>
struct studentData{
int roll;
char name[10];
};
int main(){
int i;
struct studentData st[5];
printf("Enter Records of 5 students");
for(i=0;i<5;i++){
printf("\nEnter Roll no: ");
scanf("%d",&st[i].roll);
printf("\nEnter Name: ");
scanf("%s",&st[i].name);
}
printf("\nStudent Data:");
for(i=0;i<5;i++){
printf("\nRoll no: %d, Name: %s",st[i].roll,st[i].name);
}
   return 0;
}
```

Output

```
Enter Records of 5 students
Enter Roll no: 1
Enter Name: Anushka
Enter Roll no: 2
Enter Name: Babita
Enter Roll no: 3
Enter Name: Pragati
Enter Roll no: 4
Enter Name: Ujjwal
Enter Roll no: 5
Enter Name: Prince

Student Data:
Roll no: 1, Name: Anushka
Roll no: 2, Name: Babita
Roll no: 3, Name: Pragati
Roll no: 4, Name: Ujjwal
Roll no: 5, Name: Prince
```

#### Pointer to structure

#### Structure and Functions

```c
#include<stdio.h>
#include<string.h>
struct Books{
	char title[20];
	char author[20];
	char subject[15];
	int  id;
};
void showBookData(struct Books book);
int main(){
	struct Books Book;

	/*Book Details*/
	strcpy(Book.title,"Programming in C");
	strcpy(Book.author,"Ashok N. Kamthane");
	strcpy(Book.subject,"C");
	Book.id = 120345;
	/*Calling function*/
	printf("Book Data\n");
	showBookData(Book);
	return 0;
}
void showBookData(struct Books book){
	printf("Book Title: %s\n",book.title);
	printf("Book Author: %s\n",book.author);
	printf("Book Subject: %s\n",book.subject);
	printf("Book Id: %d\n",book.id);
}
```

Output:

```
Book Data
Book Title: Programming in C Book
Author: Ashok N. Kamthane Book
Subject: C
Book Id: 120345
```

#### typedef

### Union

A union is a special data type that allows us to store different data types in the same memory location.
