---
title: Strings
date: "2020-09-20T22:40:32.169Z"
description: "Strings."
---

## String

String is actually one-dimensional charcater array terminated by null character '\0'.


#### Declaration of strings

Strings are declared in similar manner as arrays. The only difference is that, strings are of character type.

Syntax:
```c
   char str[5];
```

Strings can also be declared using pointer.

Syntax:
```c
	 char *p;
```

#### Initialization of strings

String can be intialized in different ways.

Example:
```c
	char alpha[] = "abcd";
	      OR
	char alpha[5] = "abcd";
	      OR
	char alpha[] = {'a','b','c','d','\0'};
        OR
	char alpha[5] = {'a','b','c','d','\0'};
        OR
	char *alpha = "abcd";
```


## String Manipulation Function

| SL.No | Function                            | Description                                                                                                          |
| ----- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| 1     | strlen(str)                         | computes string's length.                                                                                            |
| 2     | strcpy(str destination ,str source) | copies a string to another.                                                                                          |
| 3     | strcat(str1,str2)                   | concatenates(joins) two strings.                                                                                     |
| 4     | strcmp(str1,str2)                   | compares two strings.Returns 0 if str1 and str2 are the same; less than 0 if str1<str2; greater than 0 if str1>str2. |
| 5     | strlwr(str)                         | converts string to lowercase.                                                                                        |
| 6     | strupr(str)                         | converts string to uppercase.                                                                                        |
| 7     | strrev(str)                         | Reverse a string.                                                                                                    |
| 8     | strchr(str1, ch)                    | Returns a pointer to the first occurrence of character ch in string s1.                                              |
| 9     | strstr(str1, str2)                  | Returns a pointer to the first occurrence of string str2 in string str1.                                             |
