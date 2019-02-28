# Language basics

## Data types

### Primitive data types

Java has several primitive types built into the language. Here are some of the most common types and what they are used for.

| Type    | Description          | Examples        |
|---------|----------------------|-----------------|
| int     | Whole numbers        | `1`, `-42`      |
| double  | Decimal numbers      | `1.23`, `-0.7`  |
| char    | Single characters    | `'A'`, `'z'`    |
| boolean | True or False values | `true`, `false` |

### Strings

Although not technically a primitive data type, one of the most common data types in Java is called `String`, and it is used to represent pieces of plain text.

| Type    | Description          | Examples        |
|---------|----------------------|-----------------|
| String  | A piece of text      | `"Some words"`  |

## Variables

A key feature of Java (and, indeed, almost every programming language) is the ability to store values using _variables_. There are two things to remember about variables:

1. A variable stores a value
2. A variable must have a specific data type

You can declare a variable and assign it a value like this:

```java
int myNumber = 10;
```

You can also declare a variable without giving it a value, and give it a value later.

```java
String myString;

// Some time later...

myString = "Java is fun";
```

You are allowed to update the value of a variable multiple times:

```java
int countdown = 3;
countdown = 2;
countdown = 1;
countdown = 0;
```

## Basic operators

As you might expect, Java has a collection of basic operations that you can perform on values to do calculations and comparisons. Here are some of the most common, grouped into a few different sets.

### Arithmetic operators

Arithmetic operators can be used between values that are numbers (`int`, `double`) to perform calculations on them.

 - `+` is used for addition - `34 + 113`
 - `-` is used for subtraction - `205 - 91`
 - `*` is used for multiplication - `2 * 8`
 - `/` is used for division - `45 / 3`

One important thing to note - when performing division between two integer numbers, the result is rounded down.

For example, this means that `15 / 6` evaluates to `2`, because 6 goes into 15 two whole times (with some left over).

There is one more arithmetic operator you will come across often:

- `%` is the remainder or "modulo" operator - `15 % 6`

This is the counterpart to division - it tells you how much is left over when you try to divide one number into the other. For example, because 6 goes into 15 two whole times with three left over, `15 % 6` is equal to `3`.

### Comparison operators

You can compare two values to see which is greater or less than the other. This works for any data types which have a defined order - for instance numeric types (numbers are ordered in the way you would expect) or strings (using alphabetical order).

 - `<` is the "less-than" operator - `1 < 2`
 - `<=` is the "less-than-or-equal" operator - `3 <= 4`
 - `>` is the "greater-than" operator - `6 > 5`
 - `>=` is the "greater-than-or-equal" operator - `8 >= 7`

 These operators return a boolean value. For instance, `1 < 2` evaluates to `true`, while `5 > 6` evaluates to `false`.

 ### Equality operators

 You can also compare two values to see if they are equal.

  - `==` is the equality operator - `1 == 1`
  - `!=` is the "not-equal-to" operator - `3 != 4`

Like the comparison operators, these return a boolean value. `1 == 1` and `3 != 4` both evaluate to `true`, while `2 == 5` and `7 != 7` are both `false`.

## Input and Output

A very common task is to output some information from your program to the console, and a slightly-less-common bu still-important task is to read some input from the console.

### Output

Output a line of text with `System.out.println`. If you don't want a new line after the text you output, then use `System.out.print` instead:

```java
System.out.println("This is a line of text");
System.out.print("This will not have a new line after it");
```

### Input

The most common way to read input from the console is using a `Scanner`. Construct a `Scanner` like this:

```java
Scanner myScanner = new Scanner(System.in);
```

Use it to read input like this:

```java
// Read the next piece of text from the input, stopping at whitespace
String nextWord = myScanner.next();

// Read the entire next line of text, even if it has spaces
String nextLine = myScanner.nextLine();

// Read the next piece of text as an integer instead of a string
int nextInteger = myScanner.nextInt();
```