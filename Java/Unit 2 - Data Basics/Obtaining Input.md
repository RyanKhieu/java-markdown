Most of our programming applications will need to interact with the user. We will need to both display output to, and obtain input from, the user. We will be using a command line interface, known as the console, to obtain input.

Many authors of introductory textbooks provide their own input routines, so students can get input easily from the keyboard. Be aware that different programmers may be using different input commands.

In Eclipse, we will be using the **Scanner class** found in the **[[Packages, Objects, Methods#Packages|java.util package]]**. While there are several ways to obtain input, the Scanner class is considered the simplest method. This a relatively new class which did not exist prior to Java 1.5.0.

# Using the Scanner class
#### 1. Import the Scanner class
This class is not in the java.lang package, so you will need to import it for the program to be able to access it. Type this line at the beginning of your program, below your initial comments.
`{java}import java.util.Scanner;`
#### 2. Create a Scanner objects
We will create a variable called 'reply" (or any name you like) which is a Scanner, to take input.
`{java}Scanner reply = new Scanner(System.in);`
#### 3. Obtain and store the user input
There are several options of obtaining user data based upon the "type" of data desired.

##### A. `{java} nextInt()` If the user's response will be an integer value
The command **reply.nextInt()** will accept an integer value from the user as input. The "next integer" that is typed at the keyboard will be accepted as the input, and it will be stored in an integer variable you create.
```java
System.out.print ("Enter your desired test grade: ");
int grade = reply.nextInt();
```
(If the user types in something other than an integer, the program will crash. Be sure to type your instructions clearly so the user will understand exactly what is to be entered.)

##### B. `{java}nextDouble()` If the user's response will be a double value (decimal value)
The command **reply.nextDouble()** will accept a decimal value from the user as input. The "next double" that is typed at the keyboard will be accepted as the input, and it will be stored in a double variable you create.
```java
System.out.print ("Enter your GPA to nearest tenth: ");
String name = reply.nextDouble();
```

##### C. `{java}nextLine()` If the user's response will be text (a [[Strings|String]] value)
The command **reply.nextLine()** will accept the input. The "next line" of text that is typed at the keyboard will be accepted as the input, and it will be stored in a String variable you create.
```java
System.out.print ("Enter your full name: ");
String name = reply.nextLine(); 
```

When using the **nextLine()** method of the Scanner class, the application will wait for the user to enter text with the keyboard. The entry is completed when the user presses the Enter key. The String used to store the user's input will contain all entries, including white (blank) spaces.

The method **next()** is also an option. It will, however, only return what comes before a space. Whereas, **nextLine()** returns the entire line (spaces included) up to where the user hits Enter.

##### D. `{java}next().charAt(0)` If the user's response will be char (a single character)
There is no specific command in the Scanner class for accepting characters. To get around this problem, you can use the **next( )** in combination with **charAt(0)** to accept a single character.
```java
System.out.print ("Enter your middle initial: ");
char initial = reply.next().charAt(0);
```

#### 4. Close the Scanner object
To avoid an issue called "resource leak", close the access to the Scanner class before ending your program.
`{java}reply.close();`

If you have multiple inputs from the user of data types involving numerics (int, double) and strings (String), be sure to close the scanner at the END of the program. If you close after your first use of the first data type, the underlying stream (System.in) will get closed and your future attempts to receive input of other data types will fail (actually, you will get an error). **Once the stream (System.in) gets closed in a program, you will not be able to re-open it in that program.**

> [!WARNING]
> Confusion arises when utilizing the Scanner class with a mixture of numeric data types (int, double) with the String data type. The problem is that the newline character of the input may be left on the line to be picked up as input on the next scan for user input. Trying to scan for a String after scanning for a numeric response is the most troublesome. To avoid the confusion, you can create a new "reply" variable for each "type" of data, as shown in the example below. Or, you can include an additional **reply.nextLine();** below each input of double or int data to "eat up" the remaining newline character which is causing the problem.

It can take a while to feel comfortable with the Scanner class when working with different variable types, especially when dealing with the problem of String variables following int variable, for example. While it may not be the most efficient method, you can separate your Scanner requests (reply1, reply2, reply3) if you run into trouble. As you become more familiar with the Scanner class, you will be able to consolidate these requests and remember where the errors may occur. Check out the example below showing multiple requests, and then showing a consolidation.

```java

```