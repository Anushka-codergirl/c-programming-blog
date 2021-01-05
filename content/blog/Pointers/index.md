---
title: Pointers
date: "2020-10-04T22:40:32.169Z"
description: "Pointers are one of the strongest and also one of the most dangerous and vulnerable features of C."
---

### Pointers

A pointer is a variable that holds a memory address, usually the location of another variable in memory.

**Reference Operator(&)** is also a unary operator in c languages that uses for assign address of the variables. It returns the pointer address of the variable.

**Dereference Operator(\*)** is used to identify an operator as a pointer.

### Types of Pointers

1. NULL Pointers
2. Void Pointers
3. Wild Pointers
4. Dangling Pointers

#### NULL Pointers

It is a good practice to always assign a NULL value to a pointer variable in case we don't have exact address to be assigned. A pointer that is assigned NULL is called a null pointer. NULL pointer is a constant with a value of 0 defined in several standard libraries.

#### Void Pointers

It is also known as a general-purpose pointer.

#### Wild Pointers

Pointers that are not initialized are called wild pointers.

#### Dangling Pointers

A pointer that points to a memory location that has been deleted is called a dangling pointer.

### Pointers and Arrays

Arrays are closely related to pointers in C. Pointers and arrays are synonymous in terms of how they use to access memory. But there is a difference, that a pointer variable can take different address as value whereas, in case of array it is fixed.

```c
/*Program to find the sum of 5 numbers*/
#include<stdio.h>
int main(){
  int i, num[5], sum =0;
  printf("Enter 5 numbers:\n");
  for(i=0;i<5;i++){
    scanf("%d",(num+i));
    sum+= *(num+i);
  }
  printf("Sum = %d",sum);
  return 0;
}
```

Output:

```c
Enter 5 numbers:
11
7
2
6
7
Sum = 33
```

### Pointers and Functions
