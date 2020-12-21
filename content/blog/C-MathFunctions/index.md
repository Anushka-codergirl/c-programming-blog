---
title: C Math Functions
date: "2020-10-18T22:40:32.169Z"
description: C Math Functions.
---

### C Math Functions

C Programming allows us to perform mathematical operations. C mathematical operations are a group of functions in the standard library of the C programming language implementing basic mathematical functions. These mathematical functions are defined in **<math.h>** header file.

| SL.No. | Function              | Description                                                                                              |
| ------ | --------------------- | -------------------------------------------------------------------------------------------------------- |
| 1      | ceil(number)          | rounds up the given number. It returns the integer value which is greater than or equal to given number. |
| 2      | floor(number)         | rounds down the given number. It returns the integer value which is less than or equal to given number.  |
| 3      | sqrt(number)          | returns the square root of the given number.                                                             |
| 4      | cbrt(number)          | returns the cube root of the given number.                                                               |
| 5      | pow(base, exponent)   | returns the power of the given number.                                                                   |
| 6      | abs(number)           | returns the absolute value of the given number.                                                          |
| 7      | fabs(number)          | computes absolute value of a floating-point value.                                                       |
| 8      | div(quot,rem)         | computes the quotient and remainder of integer division.                                                 |
| 9      | fmod(number1,number2) | Computes the floating-point remainder of the division operation.                                         |
| 10     | log(number)           | computes natural logarithm (to base e).                                                                  |

```c
//Program to find square root of a number
#include<stdio.h>
#include<math.h>
int main()
{
  double num, result;

  printf("Enter a number to calculate its square root:\n");
  scanf("%lf", &num);

  result = sqrt(num);

  printf("Square root of %.2lf = %.2lf\n", num, result);

  return 0;
}
```

Output:

```c
Enter a number to calculate its square root:
12
Square root of 12.00 = 3.46
```
