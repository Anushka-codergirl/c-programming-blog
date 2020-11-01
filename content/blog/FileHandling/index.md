---
title: File Handling
date: "2020-11-01T22:40:32.169Z"
description: File Handling.
---

### File

```
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
