---
title: Command Line Arguments
date: "2020-11-08T22:40:32.169Z"
description: Command Line Arguments.
---

### Command Line Arguments

- **argc (ARGument Count)** is int and stores number of command-line arguments passed by the user including the name of the program.

- **argv(ARGument Vector)** is array of character pointers listing all the arguments.

```c
#include <stdio.h>
int main(int argc, char** argv)
{
  int i;
	printf("You have entered %d arguments\n",argc);
	for (i = 0; i < argc; ++i){
    		printf("%d",argv[i]);
  }
	return 0;
}
```
