---
title: Arrays
date: "2020-09-10T22:40:32.169Z"
description: "Array is a collection of variables of the same type that are referenced by a common name."
---

### Arrays

Array is a linear data structure. It is a collection of items stored at contiguous memory locations and elements can be accessed randomly using indices of an array.

#### One-Dimensional Arrays

A one -dimensional array is a group of elements having same datatype and same name.

```c
/*Program which will input the price of 5 items.
Calculate the total price
and apply a discount of 10% on the total amount. Display the final amount and amount after
discount.*/
#include<stdio.h>
#include<math.h>
int main()
{
    int itemprice[5],tp=0,dp,fAD,i;
    printf("Enter price of 5 items:");
    for(i=0;i<5;++i){
    	scanf("%d",&itemprice[i]);
	}
	for(i=0;i<5;i++){
		tp = tp + itemprice[i];
	}
		printf("Final amount : %d",tp);
		dp = tp * 0.10;
		fAD = tp - dp;
		printf("\nFinal amount after discount: %d", fAD);
		return 0;
}
```

Output:

```c
Enter price of 5 items:5
10
20
50
25
Final amount : 110
Final amount after discount: 99
```

#### Two-Dimensional Arrays

#### Multi-Dimensional Arrays

C allows to create array of array known as multidimensional arrays.

##### Initialization of Multidimensional Arrays

It can be initialized in different ways.

For example:

```c
int arr1[2][3] = {
	{1,3,0},
	{5,6,9}
	};

	or

int arr[][3]={
	{1,3,0},
	{5,6,9}
};

  or

int arr[2][3] = {1,3,0,6,5,8};

```

### Basic Operations on One-dimensional Arrays

- **Searching**
- **Insertion**
- **Deletion**
- **Traversal**
- **Sorting**
- **Merging**
