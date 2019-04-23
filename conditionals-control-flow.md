# Conditionals and Control Flow

In Javascript (and indeed all programming) a key feature is to be able to control the order in which the statements you write in your code are executed. This is achieved through _conditional_ statements.

## Boolean operators

Before looking at conditional statements, it's worth visiting some more common operators. These operators are those that operate on boolean values, and produce a boolean result. The three most common are:

 - `&&` is the "and" operator
 - `||` is the "or" operator
 - `!` is the "not" operator

The "and" operator returns `true` only if both of its inputs were true:

```javascript
let firstAnd = (1 === 1) && (2 === 2); // This is true
let secondAnd = (1 === 1) && (2 === 3); // This is false
```

The "or" operator returns `true` if either of its inputs is true. 

```javascript
let firstOr = (1 === 1) || (2 === 3); // This is true
let secondOr = (1 === 2) || (3 === 4); //This is false
```

The "not" operator turns `true` into `false` and `false` into `true`:

```javascript
let firstNot = !(1 === 1); // This is false
let secondNot = !(1 === 2); // This is true
```

## Conditional statements

The first and most important way you control the flow of your program is through conditional statements. Conditional statements execute different pieces of code depending on the result of a conditional expression.

### "If" statements

#### The plain "if" statement

The most common conditional statement is the "if" statement. In Javascript, it consists of three parts:

1. The `if` keyword
2. A boolean expression, contained in parentheses
3. A block of code, inside curly braces, that is executed if the boolean expression is true.

```javascript
if (9 > 2) {
    console.log("This will be displayed");
}

if (3 > 5) {
    console.log("This will not be displyed");
}
```

#### The "if-else" statement

Sometimes, if the condition of your "if" statement is not true, you want to do something else instead. You can achieve this using an augmentation of the "if" statement called "else".

1. If the boolean expression of the "if" statement evaluates to `true`, then the block of code after the "if" is executed.

2. Otherwise, if the boolean expression evaluates to `false`, then the block of code after the "else" is executed.

```javascript
if (1 === 2) {
    console.log("1 is equal to 2");
}
else {
    console.log("1 is not equal to 2");
}
```

#### The "if-elseif-else" statement

In some cases, we need to execute a separate block of code depending on multiple different boolean expressions. In that case, you can use the "if-elseif-else" statement.

1. If the expression after the "if" evaluates to `true`, then it will run the block of code that immediately follows.

2. Otherwise, if the expression after the "else if" evaluates to `true`, then it will run the block of code directly after that expression.

3. Finally, if none of the previous boolean expressions evaulate to `true`, then the block of code in the "else" block will run.

```javascript
let myScore = 2;
let yourScore = 3;

if (myScore > yourScore) {
    console.log("I beat you!");
}
else if (myScore === yourScore) {
    console.log("We drew");
}
else {
    console.log("You beat me!");
}
```

### The ternary conditional

Javascript contains a special syntax that can be shorter than an "if" statement in certain cases. it is called the "ternary" conditional. It consists of three parts:

1. A boolean expression, followed by a question mark.
2. A first alternative result that will be used if the condition is true.
3. A second alternative result that will be used if the condition is false.

The two alternatives are separated by a colon (`:`);

```javascript
let pointsScored = 19;
let gameResult = (pointsScore > 20) ? 'W' : 'L';
```

In the above code block, the boolean expression evaulates to `false`, so the second of the two alternatives (`'L'`) is used as the result of the expression.