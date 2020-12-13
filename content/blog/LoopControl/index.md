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
```c
for(initialization expression(s);test-expression;update expression(s))
{ 
//body of the loop; 
}
```

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
```c
while(expression)
{
//loop-body; 
}
```

```c
//Program to find factorial of a number
#include <stdio.h>
int main()
{
    int num,i=1,fact=1;
    printf("Enter a number: ");
    scanf("%d",&num);
    while(i<=num){
        fact = fact * i;
        i++;
    }
    printf("Factorial of %d = %d",num,fact);

    return 0;
}
```

Output:

```c
Enter a number: 6
Factorial of 6 = 720
```

#### 3. The do-While Loop

The do-while loop executes at least once when the test-expression is false initially. It executes at least once always as it evaluates the test expression at the end of the loop.
Syntax:
```c
do 
{ 
//statement; 
}while(test-expression);
```

#### 4. Nested Loop

A loop may contain another loop in its body. This type of a loop is called a nested loop.

In a nested loop, the inner loop must terminate before the outer loop terminates.


```c
//Program to print table from 1 to 10
#include<stdio.h>
int main()
{
int i,j;
for(i=1;i<=10;i++){
  {
    for(j=1;j<=10;j++)
      {
        printf("%d\t",i*j);
      }
     printf("\n");
  }
  return 0;
}
```


```c
/** * C program to print heart star pattern */ #include <stdio.h> 
int main() 
{ int i, j, n=12; 
for(i=n/2; i<=n; i+=2) 
{ 
for(j=1; j<n-i; j+=2) 
{ 
printf(" "); 
} 
for(j=1; j<=i; j++) 
{ 
printf("+"); 
} 
for(j=1; j<=n-i; j++) 
{ 
printf(" "); 
} 
for(j=1; j<=i; j++) 
{ 
printf("+"); 
} printf("\n"); 
} 
for(i=n; i>=1; i--) 
{ 
for(j=i; j<n; j++) 
{ 
printf(" "); 
} for(j=1; j<=(i*2)-1; j++) 
{ printf("+"); 
} 
printf("\n"); 
} 
return 0; 
}
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
