---
title: Decision Statements
date: "2020-08-26T22:12:03.284Z"
description: "Jump Statements"
---

### Decision Statements

#### 1. The if Statement

Syntax:

```c
if(expression){
//code to be executed
}
```

Example:

```c
#include<stdio.h>
int main()
{
	int age;
	printf("Enter your age: ");
	scanf("%d",&age);
	if(age>=18){
		printf("You are eligible to vote.");
	}
	printf("Thank you!");
	return 0;
}
```

Output:

```c
Enter your age: 18
You are eligible to vote.
Thank you!
```

#### 2. The if-else Statement

```c
if(expression){
//code to be executed if condition is true
}else{
//code to be executed if condition is false
}
```

Example:

```c
#include<stdio.h>
int main()
{
	int n1,n2;
	printf("Enter two numbers:");
	scanf("%d %d",&n1,&n2);
	if(n1>n2){
		printf("%d is greater.",n1);
	}
	else{
		printf("%d is greater.",n2);
	}
	return 0;
}
```

Output

```c
Enter two numbers:7 11
11 is greater.
```

#### 3. The if-else-if Ladder Statement

Syntax:

```c
if(condition1){
//code to be executed if condition1 is true
}else if(condition2){
//code to be executed if condition2 is true
}
else if(condition3){
//code to be executed if condition3 is true
}
else if(conditionN){
//code to be executed if conditionN is true
}
else{
//code to be executed if all the conditions are false
}
```

#### 4. The nested if-else Statement
