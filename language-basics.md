# Language basics

## Data types

Javascript has several primitive types built into the language. Here are some of the most common types and what they are used for.

| Type    | Description          | Examples        |
|---------|----------------------|-----------------|
| number  | Numbers<br/>(both whole numbers and decimal numbers) | `1`, `-42`,<br/> `1.23`, `-0.7` |
| boolean | True or False values | `true`, `false` |
| string  | A piece of text      | `"Some words"`  |


## Converting between data types

Sometimes, you will need to convert a string into a number.  
Here's how to do that:

```javascript
let myText = "4";

console.log(typeof myText);  // myText is of type "string"

let textAsNumber = +myText;  // Use + to convert a string into a number

console.log(typeof textAsNumber);  // textAsNumber is of type "number"
```

## Variables

A key feature of Java (and, indeed, almost every programming language) is the ability to store values using _variables_. There are two things to remember about variables:

1. A variable stores a value
2. You must declare (create) a variable in order to use it

You can declare a variable and assign it a value like this:

```javascript
let myNumber = 10;
```

You can also declare a variable without giving it a value, and give it a value later.

```javascript
let myString;

// Some time later...

myString = "Programming is fun";
```

You are allowed to update the value of a variable multiple times:

```javascript
let countdown = 3;
countdown = 2;
countdown = 1;
countdown = 0;
```

It's possible to change the type of the data that a variable stores  
Note: **don't do this**, because it will get confusing!

```javascript
let myData = 3;      // myData is now a number
myData = "hello";    // myData is now a string
myData = false;      // myData is now a boolean
```

### Constants

If you know your variable is never going to change, then you can declare it using `const`.  
This can be helpful, to make sure you don't accidentally change the value.

```javascript
const pi = 3.141;

pi = 3;   // This will cause an error
```

### Old ways of declaring variables

You may see Javascript code online that uses the `var` keyword.  
This is an old way of declaring variables.

```javascript
var number = 4;
```

We now use `let` instead of `var`.  
You should use `let` in your own code.

## Basic operators

As you might expect, Javascript has a collection of basic operations that you can perform on values to do calculations and comparisons. Here are some of the most common, grouped into a few different sets.

### Arithmetic operators

Arithmetic operators can be used between values that are numbers to perform calculations on them.

 - `+` is used for addition: `34 + 113`
 - `-` is used for subtraction: `205 - 91`
 - `*` is used for multiplication: `2 * 8`
 - `/` is used for division: `45 / 3`

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

  - `===` is the equality operator - `1 === 1`
  - `!==` is the "not-equal-to" operator - `3 !== 4`

Like the comparison operators, these return a boolean value. `1 === 1` and `3 !== 4` both evaluate to `true`, while `2 === 5` and `7 !== 7` are both `false`.

**Warning:**  
`===` is the equality operator.  
`==` also tests for equality, **but** if the values are of different types, it tries to coerce them into the same type.  
e.g. `3 == "3"` is true.

This can end up causing a lot of confusion, because Javascript has quite a lenient view of what is equal!  
**Remember:** always use `===`, never use `==`.

## Input and Output

A very common task is to output some information from your program to the console, and a slightly-less-common bu still-important task is to read some input from the console.

### Output

Output a line of text with `console.log`.:

```javascript
console.log("This is a line of text");
```

### Input

The best way to read input from the console is to use a package called `readline-sync`.

First, we need to install (download) the package.  
We do this by running this command on the command line in our current folder:

```bash
npm install readline-sync
```

Then, we can add this code to our program:

```javascript
// We add this line ONCE at the top of the file
// This line 'imports' the readline-sync package, so that we can use it
const readlineSync = require('readline-sync');

// Use this code to ask the user a question
// readlineSync.question returns their answer
// (which, we are storing in the variable 'answer')
let answer = readlineSync.question('What is your name? ');

console.log('Your name is: ' + answer);
```
