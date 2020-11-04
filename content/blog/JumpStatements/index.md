---
title: Jump Statements
date: "2020-09-02T22:12:03.284Z"
description: "The jump statements unconditionally transfer program control within a function."
---

### Jump Statements

The jump statements unconditionally transfer program control within a function.

#### 1. The continue Statement

The **continue** statement abandons the current iteration of the loop by skipping over the rest of the statements in the loop-body. It immediately transfers control to the evaluation of the test-expression of the loop for the next iteration of the loop.

```c
#include<stdio.h>
int main(){
  int i;
  for(i=1;i<10;i++){
    if(i%2==0){
      continue;
    }
    printf("%d",i);
  }
  return 0;
}
```

#### 2. The break Statement

The **break** statment causes the termination of the statement there and then and the control passes over to the statement following loop containing break.
A break statement can appear in any of the loops and a switch statement.

#### 3. The goto Statement

A **goto** statement transfers the program control anywhere in the program.
The target destination of a goto statement is marked by a _label_

Syntax:

```c
goto label;
.
.
.
label:
```

#### 4. The exit() Function

The **exit()** function is a library function and it breaks out of the program, abandoning the rest of the execution of the program. This function terminates the calling process immediately.