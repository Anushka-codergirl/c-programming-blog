---
title: Storage Class
date: "2020-10-16T22:40:32.169Z"
description: Storage Class.
---

### The Storage Class

#### 1.Auto

The **auto** storage class is the default storage class for all local variables.

#### 2.Extern

The **extern** storage class is used to give a reference of a global variable that is visible to all program files. When we use 'extern', the variable cannot be initialized as all it does is point the variable name at a storage location that has been previously defined.

#### 3.Static

The **static** storage class instructs the compiler to keep a local variable in existence during the life-time of the program instead of creating and destroying it each time it comes into and goes out of scope.

#### 4.Register

The **register** storage class is used to define local variables that should be stored in a register instead of RAM. This means that the variable has a maximum size equal to the register size and can't have the unary '&' operator applied to it.
