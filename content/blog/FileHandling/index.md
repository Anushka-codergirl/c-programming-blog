---
title: File Handling
date: "2020-11-01T22:40:32.169Z"
description: File Handling.
---

### File

File is a collection of bytes that is stored on secondary storage devices like disk. There are two kinds of files in a system. They are:

1. Text Files - contain ASCII codes of digits, alphabetic and symbols.
2. Binary Files - contains collection of bytes (0’s and 1’s). These are compiled version of text files.

#### File Handling Functions

| SL.No | Function  | Description                                                      |
| ----- | --------- | ---------------------------------------------------------------- |
| 1     | fopen()   | opens a file to perform operations such as reading, writing etc. |
| 2     | fclose()  | closes the file that is being pointed by file pointer fp.        |
| 3     | fgets()   | reads a file line by line.                                       |
| 4     | fprintf() | writes string into a file pointed by fp.                         |

#### Mode Of Operation Performed On A File

| SL.No | Modes | Description                                                                                                                       |
| ----- | ----- | --------------------------------------------------------------------------------------------------------------------------------- |
| 1     | r     | opens a file in read mode and sets pointer to the first character in the file. It returns null if file does not exist.            |
| 2     | w     | opens a file in write mode. It returns null if file could not be opened. If file exists, data are overwritten.                    |
| 3     | a     | opens a file in append mode. It returns null if file couldn’t be opened.                                                          |
| 4     | r+    | opens a file for read and write mode and sets pointer to the first character in the file.                                         |
| 5     | w+    | opens a file for read and write mode and sets pointer to the first character in the file.                                         |
| 6     | a+    | opens a file for read and write mode and sets pointer to the first character in the file. But, it can’t modify existing contents. |

```c
//Opening a file in read mode
#include<stdio.h>
#include<string.h>
int main()
{
	FILE *fp ;
	char dataToBeRead[50];
	// Open the existing file using fopen() in read mode using "r" attribute
	fp = fopen("file.txt", "r") ;
	// Check if this filePointer is null which maybe if the file does not exist
	if ( fp == NULL )
	{
		printf( "Failed to open the file." ) ;
	}
	else
	{
		// Read the dataToBeRead from the file using fgets() method
		while( fgets (dataToBeRead, 50, fp) != NULL )
		{
			if(ferror){
				perror(fp);

			}
			fseek(fp,2-4,SEEK_END);
			// Print the dataToBeRead
			printf("%s",dataToBeRead);
		}
		// Closing the file using fclose()
		fclose(fp) ;
	}
	return 0;
}

```

```c
//Program to Write on Data File and Read From Data File
#include<stdio.h>

struct Student {
   int roll;
   char name[12];
   int percent;
} s1 = { 1, "Anushka Raj", 82 };

int main() {
   FILE *fp;
   struct Student s2;

   //Write details of s1 to file
   fp = fopen("ip.txt", "w");
   fwrite(&s1, sizeof(s1), 1, fp);
   fclose(fp);

   fp = fopen("ip.txt", "r");
   fread(&s2, sizeof(s2), 1, fp);
   fclose(fp);

   printf("\nRoll : %d", s2.roll);
   printf("\nName : %s", s2.name);
   printf("\nPercent : %d", s2.percent);

   return (0);
}
```
