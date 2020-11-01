---
title: Structure and Union
date: "2020-10-20T23:46:37.121Z"
description: "Structure and Union"
---

### Structures

Structure is user defined data type that allows us to hold different kinds of data items. It is a collection of logically related variables referenced under one name.
Structures are used to represent a record.

#### Structure within structure

#### Array of structures

#### Pointer to structure

#### Structure and Functions

```
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
Book Title: Programming in C
Book Author: Ashok N. Kamthane
Book Subject: C
Book Id: 120345
```

#### typedef

### Union

A union is a special data type that allows us to store different data types in the same memory location.
