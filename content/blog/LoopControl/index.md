---
title: Loop Control
date: "2020-08-30T22:40:32.169Z"
description: C programming language provides loops:- for, while, do-while and nested to deal with loop control.
---

### Loop Control

#### 1. The for Loop

The for loop gathers all its loop control elements on the top of the loop.

A for loop can have multiple initialization and update expressions separated by commas.

Syntax:
`for(initialization expression(s);test-expression;update expression(s)) { //body of the loop; }`

```c
//Printing numbers using for loop
#include<stdio.h>
int main(){
  int i;
  for(i=1;i<=5;i++){
    printf("i: %d\n",i);
  }
  return 0;
}
```

Output:

```c
i: 1
i: 2
i: 3
i: 4
i: 5
```

#### 2. The while Loop

The while loop evaluates a test-expression before allowing entry into the loop.
Syntax:
`while(expression) { //loop-body; }`

#### 3. The do-While Loop

The do-while loop executes at least once when the test-expression is false initially. It executes at least once always as it evaluates the test expression at the end of the loop.
Syntax:
`do { //statement; }while(test-expression);`

#### 4. Nested Loop

A loop may contain another loop in its body. This type of a loop is called a nested loop.

In a nested loop, the inner loop must terminate before the outer loop terminates.

```c
/*Program to check if two numbers are equal, 
greater or less than to each other*/
#include <stdio.h>
int main()
{
   int num1, num2;
   printf("Enter the value of num1:");
   scanf("%d", &num1);
   printf("Enter the value of num2:");
   scanf("%d",&num2);
   if (num1 != num2)
   {
	printf("num1 is not equal to num2\n");
	//Nested if else
	if (num1 > num2)
	{
		printf("num1 is greater than num2\n");
	}
	else
	{
		printf("num2 is greater than num1\n");
	}
   }
   else
   {
	printf("num1 is equal to num2\n");
   }
   return 0;
}
```

Output:

```c
Enter the value of num1:11
Enter the value of num2:29
num1 is not equal to num2
num2 is greater than num1
```

#### 5.Infinite Loop

A loop that never ends. A loop becomes infinite loop if a condition never becomes false.
You can make an endless loop by leaving the conditional expression empty.

```c
#include <stdio.h>
int main()
{
  int i = 1;
  for( ; ; )
    {
      printf("%d\n",i);
    }
return 0;
}
```
