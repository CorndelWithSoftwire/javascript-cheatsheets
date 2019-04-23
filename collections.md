# Collections

Previously you've seen how to declare variables and assign them values:

```javascript
let x = 1;
```

What if you want to deal with an arbitrary amount of objects, all of the same type/ You can't write something like this:

```javascript
let firstNumber = 1;
let secondNumber = 2;
let thirdNumber = 3;
let fourthNumber = 4;

// This is getting out of hand!
```

Instead, Javascript provides some data types that represent a whole group of things all at once. Here are two of the most important, and how to use them.

## Array

In Javascript, we use an `array` to store a list of items. 

### Creating an array

Here's an example of creating a new (empty) array:

```javascript
let luckyNumbers = [];
```

Or, we can create an array pre-populated with values:

```javascript
let luckyNumbers = [4, 8, 15, 16, 23, 42];
```

### Adding items to an array

You can add items to an `array` using the `push()` method:

```javascript
let luckyNumbers = [4, 8, 15, 16];

luckyNumbers.push(23);
luckyNumbers.push(42);

// luckyNumbers now holds the data [4, 8, 15, 16, 23, 42]
```

### Getting items out of an array

You can get items out of an array using the `[ ]` notation:

```javascript
// Create the array just as above
let luckyNumbers = [4, 8, 15, 16, 23, 42];

// Getting numbers out of the array
let four = luckyNumbers[0];
let twentyThree = luckyNumbers[4];
```

### Inserting items into the middle of an array

You can add or remove items in the middle of an array using the `splice` method.

```javascript
splice(startIndex, numberOfItemsToDelete, itemToAdd, itemToAdd, itemToAdd, ...)
```

You use the `splice` method like this:

```javascript
let numbers = [1, 2, 3];

// Insert 4 at the beginning (index 0)
// splice(0, 0, 4) means "At index 0, delete 0 items and add the item '4'"
numbers.splice(0, 0, 4);

// numbers is now [4, 1, 2, 3]

// Insert 5 in the middle (index 2)
// splice(2, 0, 5) means "At index 2, delete 0 items and add the item '5'"
numbers.splice(2, 0, 5);

// numbers is now [4, 1, 5, 2, 3]
```

### Iterating over an array

You can iterate over every item in an array in two ways.

Firstly using a plain for-loop:

```javascript
let words = ["Lights", "Cameras", "Action"];

for (let index = 0; index < words.length; index++) {
    console.log(words[index]);
}
```

This code loops over each index from 0 to the length of the array, and for each index, gets that item from the array and prints it out.

## Objects

Obejcts in Javascript can be used a bit like a dictionary. Whereas a dictionary contains a set of words and a definition for each word, objects contains a set of _keys_ and a _value_ for each key.

When you look up a word in a dictionary, you can get the definition for that word. Similarly, when you look up a _key_ on an object, you can retrieve the _value_ associated with that key.

### Creating an object

You can create an empty object using the following code:

```javascript
let agesOfPeople = {};
```

Or, you can create an object pre-populated with values:

```javascript
let agesOfPeople = {
    "Sam": 24,
    "Tom": 22
};
```

### Adding / changing values on an object

You can add or change values on an object using the `[ ]` notation.  
We must specify the key we want to add or edit, and the value that should be associated with it.  
For example, to store the ages of some people:

```javascript
let agesOfPeople = {
    "Sam": 24,
    "Tom": 22
};

// We can add Amy's age like this:
agesOfPeople["Amy"] = 27;

// And we can change Tom's age in the same way, like this:
agesOfPeople["Tom"] = 23;
```

### Getting values out of an object

You can look up the value associated with a particular key using the `[ ]` notation:

```javascript
let agesOfPeople = {
    "Sam": 24,
    "Tom": 22
};

let samsAge = agesOfPeople["Sam"];
let tomsAge = agesOfPeople["Tom"];
```
