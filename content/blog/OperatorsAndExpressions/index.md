---
title: Operators And Expressions
date: "2020-08-23T22:40:32.169Z"
description: Operators And Expressions.
---

**Operators and Operands**
The operations (specific tasks) are represented by Operators and the objects of the operation(s) are referred to as Operand.

**Expression**
An expression in C is any valid combination of tokens.

```c
//Program to add two numbers
#include<stdio.h>
int main()
{
  int n1, n2, sum;
  printf("Enter two numbers: ");
  scanf("%d %d",&n1,&n2);
  sum = n1 + n2;
  printf("Sum = %d", sum);
 return 0;
}
```

Output:

```c
Enter two numbers: 10 15
Sum = 25
```

### Precedence of operators

The precedence of operators determines which operator is executed first if there is more than one operator in an expression.

### Associativity of Operators

The associativity of operators determines the direction in which an expression is evaluated.
