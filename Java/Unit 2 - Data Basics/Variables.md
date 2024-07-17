---
tags:
  - Variables
---
Java recognizes different data types of variables depending upon what kind of data they can contain. Java has eight built-in primitive data types designated by reserved words: **byte, short, int, long, float, double, char, Boolean**.

Variables of different types occupy different amounts of memory space and are described as having different sizes.

Of the eight primitive data types in Java, the four most commonly used are: double, int, boolean, and char. When you learn about objects, you will discuss the differences between primitives and objects.

# Definitions
- A variable is a named memory location which temporarily stores data that can change while the program is running.
- A final is a named memory location which temporarily stores data that remains the same throughout the execution of the program. It is a constant variable in the program.
- The type of a variable indicates what kind of value it will store.
- The name of a variable is known as its identifier.
- A variable is given a value through an assignment statement.

| Data Type     | Java Keyword | Kind of Value                                | Bytes of Memory | Range of Values                               |
| ------------- | ------------ | -------------------------------------------- | --------------- | --------------------------------------------- |
| Character     | **char**     | 1 character - Unicode                        | 2               | not applicable                                |
| Byte          | **byte**     | integer                                      | 1               | -128 to 127                                   |
| Short integer | **short**    | Integers                                     | 2               | -32,768 to 32,767                             |
| Integer       | **int**      | Integers                                     | 4               | -2,147,483,648 to 2,147,483,647               |
| Long Integer  | **long**     | Integers                                     | 8               | -9223372036854775808 to 9223372036854775807   |
| Float         | **float**    | Decimal values to 7 decimal digit precision  | 4               | 3.4e-38 to 3.4e38<br>positive and negative    |
| Double        | **double**   | Decimal values to 15 decimal digit precision | 8               | 1.7e-308 to 1.73e308<br>positive and negative |
| Boolean       | **bool**     | Boolean (Logical) values (True or False)     | 1               | not applicable                                |

# Rules for assigning variables:
- Assign int data types when you are sure a variable is an integer (NO decimal points). (You could also use "short" or "long", but for now we will concentrate on "int". Which type you choose would depend upon the size of the numbers.)
- Assign double when decimals are needed. (You could also use "float", but for now we will concentrate on "double". Which type you choose would depend upon the size of the numbers.)
- Assign char if the variable will always contain only ONE character of data. A char variable is a single letter, number, or symbol and is always assigned using single quotes (char letter = 'M';)
- Assign boolean if you are dealing with TRUE or FALSE situations. We will discuss these in more detail in upcoming lessons.