---
tags: Variables, Output
---
#### Java supplies the **System class** which contains methods for displaying output.

> [!INFO] Remember
> The basic output statement in Java is `{java}System.out.println( );`
>
> `{java}System.out.println(" text ");` will print what is between the double quotes " " and move the printing cursor to the next line.
>
> `{java}System.out.print(" text ");` will print what is between the double quotes and leave the printing cursor on the same line.

# When dealing with [[Variables|variables]]
```java
System.out.println("The total pay is " + totalPay);
```

What is surrounded by " " is referred to as a "literal print" and gets printed exactly as it appears. The "+" sign indicates that the value stored in the variable totalPay will be printed immediately following the literal print.

```java
double totalPay = 1006.5;
System.out.println("The total pay is " + totalPay);
```
> [!INFO] On the screen
> The total pay is 1006.5

You can print an arithmetic expression within a System.out.print statement. Use parentheses around the arithmetic expression to avoid unexpected problems.

```java
System.out.println("Adding ten to the total: " + (totalPay + 10));
```
---
Programmers that are familiar with other programming languages (such as C, C++, or Perl) are used to working with a print method known as "**printf**". The "formatting styles" of this method are reusable between languages, including Java.

A simple formatting for the "printf" method is shown below:
`{java}System.out.printf("The %s has %s, %d of them!", "dog", "fleas", 5);`

In Java, this same style of formatting used with "printf" appears in the format method:
`{java}System.out.format("The %s has %s, %d of them!", "dog", "fleas", 5);`

The **printf** method is seen by some programmers as simply a "convenience" for C/C++ programmers who are programming in Java. The **format method** is thought of as a more Java-like choice.

This site will be using the format method. See more information about using this method in the
Formatting Output lesson.