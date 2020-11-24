---
title: Dynamic Memory Allocation
date: "2020-11-10T22:40:32.169Z"
description: Dynamic Memory Allocation.
---

###Dynamic Memory Allocation

Dynamic Memory Allocation refers to allocating memory manually during run-time. It allows to solve memory issues such as increasing size, decreasing size or releasing space when no space is required.

There are four types of functions for dynamic memory allocation: -

| SL.No. | Function  | Description                                                                                  |
| ------ | --------- | -------------------------------------------------------------------------------------------- |
| 1.     | malloc()  | allocates requested size of bytes and returns a pointer first byte of allocated space.       |
| 2.     | calloc()  | allocates space for an array elements initializes to 0 and then returns a pointer to memory. |
| 3.     | realloc() | changes the size of previously allocated space.                                              |
| 4.     | free()    | deallocate the previously allocated space.                                                   |

#### malloc()

It stands for **memory allocation**. This function reserves a block of memory of specified size and return a pointer of type void which can be casted into pointer of any form.

Syntax:

```c
ptr = (data type *) malloc(byte size);
```

```c
/*
Program to find sum of n elements entered by user using malloc() function.
*/
#include<stdio.h>
#include<stdlib.h>
#include<process.h>
int main(){
  int *ptr, n, i, sum=0;
  printf("Enter number of elements:");
  scanf("%d",&n);
  ptr = (int *) malloc(n * sizeof(int));
  if(ptr==NULL){
    printf("Error!\nMemory not Allocated.");
    exit(0);
  }
  printf("Enter elements values:");
  for(i=0;i<n;i++){
    scanf("%d",ptr+i);
    sum += *(ptr+i);
  }
  printf("Sum = %d",sum);
  return 0;
}
```

#### calloc()

It stands for **contiguous allocation**. This function allocates multiple blocks of memory each of same size and sets all bytes to 0.

Syntax:

```c
ptr = (data type *) calloc(n,element-size);
```

#### realloc()

It stands for **re-allocation**. This function is used to enlarge or shrink the size of the previously allocated memory.

Syntax:

```c
ptr = realloc(ptr,new-size);
```

#### free()

This function is used to deallocated memory or release space.

Syntax:

```c
free(ptr);
```
