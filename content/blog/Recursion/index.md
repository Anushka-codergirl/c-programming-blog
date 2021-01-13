---
title: Recursion
date: "2020-09-08T22:40:32.169Z"
description: "It is simply the process of repeating items in a self-comparable way."
---

### Recursion

It is simply the process of repeating items in a self-comparable way. In recursion, function calls itself directly or indirectly.
Recursive functions are very useful to solve many mathematical problems, such as calculating the factorial of a number, generating Fibonacci series, etc.

#### Types of Recursions:

1.Direct Recursion
If a function calls itself, it’s known as direct recursion. This results in a one-step recursive call: the function makes a recursive call inside its own function body.
2.Indirect Recursion
If the function f1 calls another function f2 and f2 calls f1 then it is indirect recursion (or mutual recursion).
This is a two-step recursive call: the function calls another function to make a recursive call.

```c
#include <stdio.h>
 
int sum (int);
 
int main()
{
    int num, result;
 
    printf("Enter the number: ");
    scanf("%d", &num);
    if(num>0){
    	printf("The given number is positive.\n");
    	result = sum(num);
   		printf("Sum of digits of %d is %d\n", num, result);
	} 
	else if(num==0){
		result = sum(num);
		printf("Sum of digits of %d is %d\n", num, result);
	}
	else{
		printf("Please enter positive 5-digit number...\nThank you!");	
	}
    return 0;
}
 
int sum (int num)
{
    if (num>0)
    {
    	return (num % 10 + sum(num / 10));    
    }
    else
    {
       return 0;
    }
}
```

Output:

```c
Enter the number: 12436
The given number is positive.
Sum of digits of 12436 is 16
```
