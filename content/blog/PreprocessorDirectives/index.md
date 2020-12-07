---
title: Preprocessor Directives
date: "2020-10-24T22:40:32.169Z"
description: Preprocessor Directives.
---

Preprocessor Directives

#### The #define Directive

```c
/* Fahrenheit to Celcius conversion table*/
#include<stdio.h>
#define LOWER 0
/* lower limit of temp. table (in Fahrenheit) */
#define UPPER 300
/* upper limit */
#define STEP 20
/* step size */
int main(void){
int fahr;
for (fahr = LOWER; fahr <= UPPER; fahr += STEP)
printf("%3d \t%6.1f\n", fahr, (5.0/9.0) * (fahr−32.0));
}
```

```c
//Area of circle using #define preprocessor
#include <stdio.h>
#define PI 3.14
#define AreaofCircle(r) (PI*r*r)

int main() {
    float radius, area;
    printf("Enter the radius: ");
    scanf("%f", &radius);
    area = AreaofCircle(radius);
    printf("Area = %.2f", area);
    return 0;
}
```
