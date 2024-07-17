---
tags: Output
---
Formatting options are of particular benefit when creating charts or tables of information. There are a variety of ways to format data in Java.

The **format() method** can be used instead of **print()** or **println()** to control the way your display will look. A **format()** provides a "template" of how the spacing of your information will occur. This template is called the format string specifier, and takes the form:
### % \[alignment] \[width] s
% indicates that the specifier (template) is starting, for each section
\[alignment] implies right alignment. Include (-) for left alignment.
\[width] is the number of characters to use for output
s indicates that the corresponding argument is a [[Strings|string]]

**format()** behaves similar to print() in that it will leave you on the same line, and will not move down to the next line. You will need to force a "\\n" at the end of each line to move to the next line.

If **\[width]** is larger than the number of characters in the corresponding string, then extra spaces will pad the output. If \[width] is smaller than the number of characters in the corresponding string, will be displayed and any strings to the right will be moved over.

> [!EXAMPLE] Example 1
> ```java
> public class testing {
> 	public static void main(String[] args) {
> 		System.out.format("%-10s %8s %8s", "Class", "Girls", "Boys\n");
> 		System.out.format("%-10s %8s %8s", "Freshman", "50", "62\n");
> 		System.out.format("%-10s %8s %8s", "Sophomore", "60", "70\n");
> 		System.out.format("%-10s %8s %8s", "Junior", "58", "63\n");
> 		System.out.format("%-10s %8s %8s", "Senior", "44", "52\n");
> 	}
> }
> ```
>
> **Display:**
> ```
> Class        Girls    Boys
> Freshman     50       62
> Sophomore    60       70
> Junior       58       63
> Senior       44       52
> ```

> [!EXAMPLE] Example 2 (You can also mix the printing of "normal text" within the format string.)
> ```java
> public class testing {
> 	public static void main(String[] args) {
> 		System.out.format("The x-coordinates could be: %3s %3s", "-2", "3");
> 	}
> }
> ```
>
> **Display:**
> ```
> The x-coordinates could be:  -2   3
> ```

**It is also possible to use the format() method** to format numeric values. For **floating point numbers** a specifier can take the form:
### %\[alignment]\[width]\[.decimal]f
% indicates that the specifier (template) is starting, for each section.
\[alignment] implies right alignment. Include (-) for left alignment.
\[width] is the number of characters to use for output.
f indicates the corresponding argument is floating point number.

For **integer values** a specifier can take the form:
### %\[alignment]\[width]d
% indicates that the specifier (template) is starting, for each section.
\[alignment] implies right alignment. Include (-) for left alignment.
\[width] is the number of characters to use for output.
d indicates that the corresponding argument is an integer value.
Be careful! "d" stands for "integer", not "double".

If numeric values exceed the formatting number of decimal digits, normal mathematical **rounding** will occur.

> [!EXAMPLE] Example 3 (floating point, doubles)
> ```java
> public class testing {
> 	public static void main(String[] args) {
> 		double x = 2.5, y = 5.78;
> 		System.out.format("%15.2f %15.2f", x, y);
> 	}
> }
> ```
> 
> **Display:**
> ```
>            2.50            5.78
> ```
> 
> Notice how the %15.**2**f prints 2 decimal places.

> [!EXAMPLE] Example 4 (integers)
> ```java
> public class testing {
> 	public static void main(String[] args) {
> 		int x = 3, y = 4;
> 		System.out.format("%3d %3d", x, y);
> 	}
> }
> ```
> 
> **Display:**
> ```
>   3  4
> ```
