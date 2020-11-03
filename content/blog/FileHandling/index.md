---
title: File Handling
date: "2020-11-01T22:40:32.169Z"
description: File Handling.
---

### File

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
