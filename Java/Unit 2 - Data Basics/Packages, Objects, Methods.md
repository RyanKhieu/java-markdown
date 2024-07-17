Object-Oriented Programming (OOP) developed out of a need for complex programs to be designed in a modular fashion where programmers could create "modules" that would be used over and over in a variety of programs. In addition to object-oriented capabilities, the Java language can also be used for *platform-independent applications* that can be run on any computer, making it a widely received language.

When programming in an object-oriented language, you are working with **objects**, **classes**, and **packages**. The diagram below will give you a general idea of how these concepts are related to one another.

![[Screenshot 2024-07-11 at 4.03.02 AM.png]]

# Packages
The API (*Application Programming Interface*) provides all of the classes that are included as part of the JDK (*Java Development Kit*). In your study of Java, you will utilize many of the different Java classes.

The Java SE API stores classes in packages. We will be using three of the most common packages in this unit.
1. The **java.lang package** contains the classes that are the most fundamental to the Java language. As a result, this package is automatically available to all Java code and requires no action (**no importing**) on the part of the programmer. The String class, for example, is in this package.
2. The **java.util package** contains utility classes, such as those needed to obtain input from the user through the console (keyboard). This package **needs to be imported** to access its classes. We will be using the "Scanner class" in this package to obtain keyboard data from the user.
	`{java} import java.util.Scanner;`
3. The **java.text package** contains classes that deal with text manipulation, including those for formatting numbers, dates and amounts of money. This package **needs to be imported** to access its classes. We will be using the "DecimalFormat class" in this package to control the output of decimal entries, including money.
	`{java}import java.text.DecimalFormat;` or `{java}import java.text.*;`

When you import a package, you can import ONLY the class you are interested in using by specifying its name, or you can import ALL of the classes in the package by using an asterisk (\*) in place of a specific class name. You will see us using both approaches in the next few lessons.

While it may seem easier to always import ALL of the classes (just to cover all of your bases), it can cause problems. For example, a "Date class" exists in more than one package. If you should import all classes from both of these packages, the computer would not know which Date class it should be using.

# Objects & Methods
To use a Java class, you typically need to create an object from the class. When dealing with the Scanner class, we will create an **object** called *reply*.
`{java}Scanner reply = new Scanner (System.in);`

> [!INFO]
> The process of creating an object is called instantiation. System.in specifies getting input from the console.

Now, you are ready to call the methods of the object using a dot operator. We can get a line of input text from a user at the keyboard by using the **method**, *nextLine*.
`{java}String answer = reply.nextLine();`

We will be primarily working with a **Java application**, which is a **package** with at least one class that contains a **main() method**. You will notice that we will be *importing* other packages, as mentioned above, that will assist us in preparing our programming solutions.