---
title: Functions
date: "2020-09-04T23:46:37.121Z"
description: "A function is a block of statements that performs a specific task."
---

Wow! I love blogging so much already.

### Function

A **function** is a named unit of a group of program statements that can be invoked from other parts of the program as and when required.

**Function Prototype** : A function prototype is a declaration of the function that tells the program about the type of the value returned by the function and the number and type of each argument.

#### Types of function

###### 1. Built-in Function

###### 2. User-defined Function

##### Function without arguments and return

```c
#include<stdio.h>
void sum();
int main(){
   sum();
   printf("Function terminated successfully....");
   return 0;
}

void sum(){
    int num1, num2, res;
    printf("Enter two numbers: ");
    scanf("%d %d",&num1, &num2);
    res = num1 + num2;
    printf("\nResult = %d\n",res);
}
```

Output:

```c
Enter two numbers: 11
99
Result = 110
Function terminated successfully....
```

##### Function without arguments but return

##### Function with arguments but no return

```c
/* Program to print reverse of all the numbers from m to n using functions with arguments and no return type. the inputs in the program will be m and n variables and need to take these variables as arguments.*/
#include<stdio.h>
void Reverse(int,int);
int main(){
	int m, n;
	printf("Enter two arguments:");
	scanf("%d %d",&m,&n);
	Reverse(m,n);
	return 0;
}

void Reverse(int m, int n){
	int i;
	for(i=m;i<=n;i++){
		int num = i,rem=0,rev=0;
		while(num!=0){
			rem = num%10;
			rev = rev * 10 + rem;
			num/=10;	
	}	
	printf("Reverse of %d = %d\n",i,rev);
	}
}
```

Output:
```c
Enter two arguments:121
131
Reverse of 121 = 121
Reverse of 122 = 221
Reverse of 123 = 321
Reverse of 124 = 421
Reverse of 125 = 521
Reverse of 126 = 621
Reverse of 127 = 721
Reverse of 128 = 821
Reverse of 129 = 921
Reverse of 130 = 31
Reverse of 131 = 131
```

##### Function with arguments and return

#### Call by value

In call by value, the called function creates its own copies of original values sent to it. Any changes, that are made, occur on the function's copy of values and are not reflected back to the calling function.

#### Call by reference

In call by reference, the called function accesses and works with the original values using their references. Any changes, that occur, take place on the original values and are reflected back to the calling function.
