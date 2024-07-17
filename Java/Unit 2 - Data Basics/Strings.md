---
tags: Strings
---
A **string** is a sequence of multiple characters, such as letters, numbers, punctuation marks, and/or special characters. They are referred to as **alphanumerics** (alphabet characters and/or numbers.)

**The String Class** is provided by Java to allow for the discussion and use of String variables. In Java, strings are objects, not primitive types such as int, double, char, and boolean. As such, you must capitalize String since it is the name of a class.

The term **string literal** refers to any alphanumeric (character, digit, or both) enclosed in double quotation marks (such as "Snoopy" or "123 West Third Street").

> [!WARNING]
> If a string literal contains only numeric digits ("1234"), **it is still NOT a number**. Be careful! It is just a string of numeric digits that cannot be used to perform mathematical calculations such as addition or multiplication. Remember that you can perform calculations on numeric data only, not on string literals. **"1234"** is not the same as **1234**. **"1234"** is a **string**, but **1234** is a **number**.

# Declaring a String [[Variables|variable]]
is different from declaring an int, double, char or boolean. The variable name of a String holds the **address** of the memory location where the actual body of the string is stored.
![[Pasted image 20240709032441.png]]
Each time a new assignment is stored in the String variable "name", the computer finds a new memory location to hold the String text and adjusts the contents of "name" to hold the address of this new location. The old memory location is set free.

Variable used in the manner (such as "name") are called **references**. The address values stored in these variables are said to "point" to the actual data.

> [!NOTE]
> The string object in memory is made up of individual characters (chars) as shown below. These characters are indexed starting with the number zero. Notice that the index of the last char is one less than the actual length of the string.

These indexes will be used to access "parts" of the string variable, as seen in the [[#String Methods]] section below.
![[Screenshot 2024-07-09 at 5.08.29 PM.png]]

If you assign a null to a string, use the null keyword. The String variable will not point to a String object that's allocated memory. `{java}String variable = null;`
Do not confuse the null string with an empty string. `{java}String variable = “”;`
The empty string is coded with a set of quotations marks with no space between them. This String variable is known, but the string does not contain any characters.

> [!EXAMPLE] Example A
> ```java
> String greeting; //declare the string
> greeting = "Hello"; //initialize the string
> ```

> [!EXAMPLE] Example B
> ```java
> String title = "captain" //declare and initialize at once
> System.out.println(title); //print
> ```

> [!EXAMPLE] Example C
> ```java
> String poem = scan.nextLine();
> ```
> This code will read all the characters a user types up to the pressing of the Enter key. This input process will be examined further in the next lesson.

# Printing String Variables
The statement below was seen in the Printing section. We now know that the "literal print" in this statement is in fact a "string literal".
`{java}System.out.println(" The total pay is " + totalPay);`

The + (plus) operator that we saw at work in the statement above is part of a process referred to as concatenation. **Concatenation** is the combining or merging of two String fields using the + operator. In the statement above, the "+" sign concatenates the string literal with the value that is stored in the variable totalPay. While totalPay is declared as a double in the program, it is automatically converted to a String for the purpose of concatenation and the subsequent print out.

> [!EXAMPLE]
> ```java
> String firstName = "Darth";
> String lastName = "Vader";
> System.out.println(firstName + " " + lastName);
> ```
> Prints to screen: Darth Vader
>
> Notice the need of the " " (blank space) to separate the first name from the last name.

**Potential problem concatenating Strings with numerics:**

```java
System.out.println("answer " + 3 + 4); // becomes answer 34
System.out.println("answer " + (3 + 4)); // becomes answer 7
```

As suggested in the Printing section, placing numeric values in parentheses will help avoid this order of operations problem with the "+".

The concatenation operator (+) has the same precedence as addition, which may occasionally cause strange results.

# String Methods
String is a "class" and as such has methods that are properties of the class. To use a method, we need the dot operator.

#### 1. length()
This is a numerical returning method that gives the length of the string. It returns an integer value.

> [!EXAMPLE]
> ```java
> //store the length of a city name into an int
> int citylength = city.length();
> //print length
> System.out.println(citylength);
> ```

#### 2. charAt(n)
This is a value returning method. The argument states which character to return. The subscripting of the locations of the characters starts with zero.

> [!EXAMPLE]
> ```java
> String holiday = "Thanksgiving";
> System.out.println(holiday.charAt(4));
> //prints out a 'k'
> ```

> [!EXAMPLE]
> ```java
> String puppy ="Wally";
> System.out.println(puppy.charAt (0));
> //prints out a 'W'
> ```

#### 3. trim( )
This is a value returning method that returns a copy of the argument after removing its leading and trailing blanks (not embedded blanks - blanks within the statement). The string will not be changed in memory.

> [!EXAMPLE]
> ```java
> String burp = "      hic up      ";
> System.out.println(burp.trim()); // prints hic up
> ```

#### 4. toLowerCase( )
In memory, the string is not changed, but it will be printed out in all lower case letters.

> [!EXAMPLE]
> ```java
> String cityname = "Houston";
> System.out.println(cityname.toLowerCase());
> // prints out houston
> ```

#### 5. substring(Start, End)
This is a value returning method. A string is returned beginning at **Start** subscript up to but not including the **End** subscript.

> [!EXAMPLE]
> ```java
> String sport = "football";
> System.out.println(sport.substring(1,3));
> // prints out oo
> ```

#### 6. substring(Start)
This is an alternate version. It returns the substring beginning at **Start subscript** up to and including the end of the string.

> [!EXAMPLE]
> ```java
> String sport = "football";
> System.out.println(sport.substring(1));
> // prints out ootball
> ```

#### 7. indexOf("Garfield")
Returns the beginning subscript of the string where "Garfield" is found.

> [!EXAMPLE] Example (find comma in a city, state, zip listing)
> ```java
> String city = "Fulton, New York 13069";
> System.out.println(city.indexOf(","));
> // prints 6
> ```

#### 8. equals( )
Used to compare two strings with the method to see if they are exactly the same, this includes any blanks or spaces within the string.

> [!EXAMPLE] Example (check if the user entered name Snoopy)
> ```java
> if (dogname.equals("Snoopy") {
> 	System.out.println("User typed Snoopy.”);
> }
> ```

#### 9. compareTo( )
Compares strings to determine alphabetic location. Returns a zero if the two strings are equal, a negative if the first string is alphabetically before the compared string, and a positive if the first string is alphabetically after the compared string.

> [!EXAMPLE]
> ```java
> String subject = "mathematics";
> boolean answer;
> answer = subject.compareTo("biology"); // answer is positive – math comes after biology
> answer = subject.compareTo("philosophy"); // answer is negative – math comes before philosophy
> answer = subject.compareTo("mathematics"); // answer is zero – math is math
> ```
