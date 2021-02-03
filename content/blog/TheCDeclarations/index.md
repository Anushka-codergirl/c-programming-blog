---
title: The C Declarations
date: "2020-08-20T22:40:32.169Z"
description: The C Declarations.
---

### The C Declarations

####Character set

A character set is a set of valid characters that a language can recognise.
C has the following character set:

- _Letters_ A-Z ,a-z
- _Digits_ 0-9
- _Special Symbols_ + - \\\\\\\\\\\\\\\\\* / % () []{}\ / = !<> . , ; : & ^ ? \\\\\\\\\\\\\\\\\_ ' " ~ # \$
- _White Spaces_ Blank Space, Horizontal tab, Carriage return, Newline, Form feed.

**Token**: It is the smallest individual unit in a program.

**Keywords**: These are the preserved words that convey a special meaning to the language compiler. It cannot be used as variable names because that would try to change the existing meaning of the keyword, that is'nt allowed.

List of keywords :-

|          |          |          |        |
| :------: | :------: | :------: | :----: |
|   auto   |  break   |   case   |  char  |
|  const   | continue | default  |   do   |
|  double  |   else   |   enum   | extern |
|  float   |   for    |   goto   |   if   |
|   int    |   long   | register | return |
|  short   |  signed  |  sizeof  | static |
|  struct  |  switch  | typedef  | union  |
| unsigned |   void   | volatile | while  |
| \_packed |

**Identifier** : It is the name given by user for a unit of the program i.e. variables, constants, functions and user-define data.

####Rules for an Identifier

- An Identifier can only have alphanumeric characters(a-z , A-Z , 0-9) and underscore(\_).
- The first character of an identifier can only contain alphabet(a-z , A-Z) or underscore (\_).
- Identifiers are also case sensitive in C. For example name and Name are two different identifiers in C.
- Keywords are not allowed to be used as Identifiers.
- No special characters, such as semicolon, period, whitespaces, slash or comma are permitted to be used in or as Identifier.

**Literals**: These (often referred to as contants) are data items that never change their value during a program run.

### Data Types

Data types refer to an extensive system used for declaring variables or functions of different types.

## 1. Basic Types

These are of three types:

- **integer types**
- **floating-point types**
- **character types**

## 2. Derived Types

They include

- **Array**
- **Pointer**
- **Structure**
- **Union**
