# Java for Beginners

📖 A basic tutorial for Java which I complied from internet
  
- Basics
  - [Introduction to Java](#introduction_to_java)
    - [Introduction to Java](#introduction_to_java)
    - [Basic literals](#basic_literals)
    - [Overview of the basic program](#overview_of_the_basic_program)
    - [Printing data](#printing_data)
  - [Data types and variables](#data_types_and_variables)
    - [Types and variables](#types_and_variables)
    - [Sizes and ranges](#sizes_and_ranges)
    - [Type casting](#type_casting)
    - [Primitive and reference type](#primitive_and_reference_type)
    - [Final variables](#final_variable)
    - [Types of references](#types_of_references)
    - [Floating-point types](#floating_point_types)
    - [Numeric literals](#numeric_literals
  - [Simple programs](#sample_programs)
  - [Operations on primitive types](#operations_on_primitive_types)
  - [Control flow statements](#control_flow_statements)


## Basics

### Introduction to Java <a name="introduction_to_java"></a>

#### What is Java?

**Java** is a general-purpose modern programming language initially developed by [Sun Microsystems](https://en.wikipedia.org/wiki/Sun_Microsystems), and currently owned by [Oracle Corporation](https://en.wikipedia.org/wiki/Oracle_Corporation "Link: https://en.wikipedia.org/wiki/Oracle_Corporation"). The key feature of the language is **platform independence**: it means that the same Java program can be run on multiple platforms without any changes! This principle is also known as *"write once, run anywhere"* (or *WORA*).

Java has been one of the most popular programming languages for many years. It has earned the top position in the [TIOBE](https://www.tiobe.com/tiobe-index/) index (a programming language popularity index). This language is used by a huge community of developers around the world! If you have a problem, you can always ask other developers or find a suitable answer online.

Java is used in our **Android** smartphones, the financial services industry, telecommunications, embedded systems, and in many other areas. Medical applications use it to store patient data, computer games, such as Minecraft, are created using Java; development tools like IntelliJ IDEA and Eclipse wouldn't exist without it.

#### A short history of Java

The Java language project was initiated in 1991 by James Gosling and his colleagues. In the beginning, the language was called "Oak." Later the project was renamed "Java" as a reference to Java coffee. For this reason, the language’s logo is a cup of coffee.

<img src="https://ucarecdn.com/6b2b0c7a-8b69-4701-947c-b869bef018ba/" title="Java Logo" alt="Java Logo" data-align="center">

**The logo of the Java language**

Sun Microsystems released Java 1.0 in 1996. After that, new versions were released every 1 to 3 years. Since Java 9, released in 2017, new versions have been released every 6 months. You can read more about its history and find the most recent version [here](https://en.wikipedia.org/wiki/Java_version_history).

#### Some important features of Java

As we've mentioned before, the most important feature of Java is **platform independence**.

Another important feature is a **simple** and **clear syntax**. Many elements of the language are easy to read and are widely used in other programming languages such as C/C++, C#, JavaScript, and Go.

If you have ever written programs in C/C++, you know that manual memory cleaning can lead to bugs in the code. Fortunately, Java has a **garbage collector** that **automatically cleans memory** from unused objects during runtime.

It is also important to note that Java supports multiple programming paradigms; you will get to know more about them in future topics. Java is primarily an imperative language based on the object-oriented concept: almost every part of a program is an object. Therefore, a program itself can be considered as a set of interacting objects. Also, it partially supports modern programming paradigms such as *generic programming, concurrent programming, functional programming*, and some others.

> If you are a beginner in programming, it may be difficult to comprehend all the features of Java right now. This is not a bad thing. Throughout this set of topics, you will learn about all of these concepts. Also, Java has comprehensive [online documentation](https://docs.oracle.com/en/java/javase/11/) that comprises guides, tutorials, specifications, API documentation, technical information, and more. We will refer you to it from time to time during your studies.

In conclusion, Java is a modern and popular programming language that can be successfully used in almost all domains.

### Basic literals

#### Literals

Regardless of its complexity, a program always performs operations on numbers, strings, and other values. These values are called **literals**. There are many different sorts of literals in Java, but in this topic we will focus only on a few of them: the ones that surround us all the time in everyday life.

Let's consider integer numbers, strings, and characters in the format in which they are written in Java.

#### Integer numbers

These numbers are used to count things in the real world. Also, we will often use them in Java.

Here are several examples of valid integer number literals separated by commas: `0, 1, 2, 10, 11, 100`.

If an integer value contains a lot of digits, we can add underscores to divide the digit into blocks for increased readability: `1_000_000`. It's more readable than the same value written as `1000000`.

#### Characters

A single character can represent a digit, a letter or another symbol. To write a character we use single quotes as follows: `'A', 'B', 'C', 'x', 'y', 'z', '0', '1', '2', '9'`. Character literals can represent symbols of an alphabet, digits from `'0'` to `'9'`, whitespaces (`' '`), or other characters or symbols (`'$'`).

Do not confuse characters that represent numbers (e.g. `'9'`), with numbers themselves (e.g. `9`).

A character can't include two and more digits or letters because it represents only a single symbol. The following two examples are **incorrect**: `'abc', '543'`. These literals contain too many characters.

#### Strings

A string is a sequence of any individual characters. Strings represent text information such as a text of advertising, an address of a web page or a login on a site.

To write a string we use double quotes instead of single ones. Here are some valid examples: `"text", "I want to know Java", "123456", "e-mail@gmail.com"`. A string consisting of a single character like `"A"` is also a valid string, but do not confuse it with the `'A'` character.

As you can see, strings can include letters, digits, whitespaces, and other characters.

#### Remember

Do not confuse these literals:

- `123` is an integer number, `"123"` is a string;
- `'A'` is a character, `"A"` is a string;
- `'1'` is a character, `1` is an integer number.

### Overview of the basic program

In this topic, we will build our very first Java program. Our program will simply print **"Hello, World!"** on the screen (a tradition by most programmers when learning new languages). Our code may not seem too exciting at first, however, we will learn about the basic template that all Java programs need to follow.

#### The Hello World program

Here is the Java code of this program:

```java
public class Main {
    public static void main(String[] args) {        
        System.out.println("Hello, World!");    
    }
} 
```

You can type this code in the **Your Code** section [here](https://www.jdoodle.com/online-java-compiler) and then press the **execute** button. In the **result** section, you will see:

```java
Hello, World!
```

If you have already installed Java, you can run the program on your computer. If not, there is no need to install it right now. We will do that later.

#### The basic terminology

Now that you have seen the result, let's learn some basic terminology and then try to understand this program.

- **Program** – a sequence of instructions (called statements), which are executed one after another in a predictable manner. Sequential flow is the most common and straightforward sequence of statements, in which statements are executed in the order that they are written – from top to bottom in a sequential manner;
- **Statement** – a single action (like print a text) terminated by semi-colon (`;`);
- **Block** – a group of zero, one or more statements enclosed by a pair of braces `{...}`; There are two such blocks in the program above.
- **Method** – a sequence of statements that represents a high-level operation (also known as subprogram or procedure).
- **Syntax** – a set of rules that define how a program needs to be written in order to be valid; Java has its own specific syntax that we will learn;
- **Keyword** – a word that has a special meaning in the programming language (`public`, `class`, and many others). These words cannot be used as variable names for your own program;
- **Identifier or name** – a word that refers to something in a program (such as a variable or a function name);
- **Comment** – a textual explanation of what the code does. Java comments start with `//`.
- **Whitespace** – all characters that are not visible (space, tab, newline, etc.).

#### The Hello World program under a microscope

The **Hello World** program illustrates the basic elements of Java programs. For now, we will discuss only the most important elements.

1. **The public class.** It is the basic unit of a program. Every Java program must have at least one class. The definition of a class consists of the `class` keyword followed by the class name. A class can have any name, such as `App`, `Main`, or `Program`, but it must not start with a digit. A set of braces `{...}` encloses the body of a class.

```java
public class Main {    
    // ...
}
```

The text after `//` is just a comment, not a part of the program. We will learn about comments in detail in later topics.

**2. The main method.** To make the program runnable, we put a method named `main` inside a class. It is the entry point for a Java program. Again, the braces `{...}` enclose the body of the method, which contains programming statements.

```java
public static void main(String[] args) {    
    // statements go here
}
```

The keywords `public`, `static`, and `void` will be discussed later, so just remember them for now. The name of this method (`main`) is predefined and should always be the same. Capitalization matters; if you name your first method like **Main**, **MAIN** or something else, the program cannot start.

The element `String[] args` represents a sequence of arguments passed to the program from the outside world. Don't worry about them right now.

**3. Printing "Hello, world!"**. The body of the method consists of programming statements that determine what the program should do after starting. Our program prints the string **"Hello, World!"** using the following statement:

```java
System.out.println("Hello, World!"); //  each statement has to end with ;
```

This is one of the most important things to understand from the **Hello World** program. We invoke a special method `println` to display a string followed by a new line on the screen. We will often use this approach to print something of interest to the screen. The text is printed without double quotes.

> It is important that **"Hello, World!"** is not a keyword or an identifier; it is just a text to be printed.

#### Keywords

As you can see, even a simple Java program consists of many elements, including **keywords** that are parts of the language. In total, Java provides more than 50 keywords which you will gradually learn on this platform. The full list is [here](https://en.wikipedia.org/wiki/List_of_Java_keywords), though you don't need to remember all of them at this moment.

> Note, `main` is outside the given list because it is not a keyword.

#### Conclusion

We have discussed the simplest program you can write in Java. It has a single class with a single `main` method. Every Java program must have a `main` method as it is the first to be executed when the program runs. Don't worry about memorizing every single term used in the topic (syntax, statement, block). These terms will reappear in further materials. Do not forget to use the provided **Hello World** program as a template for your own programs.

### Printing data

When you write programs, you often need to print calculation results, text, or any other type of data. Also, throughout this educational platform, you will write a lot of programs that print data on the screen. Let's learn how to do that using a standard approach in Java.

#### Displaying text using println() and print()

**Standard output** is a receiver to which a program can send information as text. It is supported by all common operating systems. Java provides a special `System.out` object to work with the standard output. We will often use it to print data.

The `println` method displays the passed string followed by a new line on the screen (**print-line**). For example, the following code snippet prints four lines.

```java
System.out.println("I ");
System.out.println("know ");
System.out.println("Java ");
System.out.println("well.");
```

Here is the output we get:

```no-highlight
I 
know 
Java 
well.
```

All the strings were printed as they are, without double quotes.

This method allows you to print an empty line when no string is given:

```java
System.out.println("Java is a popular programming language.");
System.out.println(); // prints empty line
System.out.println("It is used all over the world!");
```

And here is the output:

```no-highlight
Java is a popular programming language.

It is used all over the world!
```

The `print` method displays the value that was passed in and places the cursor (the position where we display a value) after it. For example, the code below outputs all strings in a single line.

```java
System.out.print("I ");
System.out.print("know ");
System.out.print("Java ");
System.out.print("well.");
```

We receive the following output:

```no-highlight
I know Java well.
```

Pay attention to the spaces between words. We pass them to methods for printing.

#### Printing numbers and characters

Both `println` and `print` methods allow a program to print not only strings and characters, but also numbers.

Let's print two secret codes.

```java
System.out.print(108);   // printing a number
System.out.print('c');   // printing a character that represents a letter
System.out.print("Q");   // printing a string
System.out.println('3'); // printing a character that represents a digit

System.out.print(22);
System.out.print('E');
System.out.print(8);
System.out.println('1');
```

Here is our output:

```no-highlight
108cQ3
22E81
```

As is the case with strings, none of the characters contain quotes.

#### Conclusion

In Java, you can print data via standard output using the `System.out` object. You can use `println` method to display the passed string in a print-line and the `print` method to output all passed strings in a single line. Both of these methods also allow for printing numbers as well as characters.

## Code Organization

### Code Style

## Working with Data

## Errorless Code

## Java Internals

## Additional Instruments
