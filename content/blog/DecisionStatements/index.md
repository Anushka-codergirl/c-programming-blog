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
