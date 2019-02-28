# Collections

Previously you've seen how to declare variables of a particular type and assign them values:

```java
int x = 1;
```

What if you want to deal with an arbitrary amount of objects, all of the same type/ You can't write something like this:

```java
int firstNumber = 1;
int secondNumber = 2;
int thirdNumber = 3;
int fourthNumber = 4;

// This is getting out of hand!
```

Instead, Java provides some data types that represent a whole group of things all at once. Here are two of the most important, and how to use them.

## List

In Java, the `List` stores a sequential list of data of a specified type. 

### Creating a List

Here's an example of creating a new (empty) list that will hold integer values:

```java
List<Integer> scores = new ArrayList<>();
```

The type that goes in between the angle brackets (in this case `Integer`) is the type of object that will go in our list. Since we want a list of integers, we use the `Integer` type.

### Adding items to a List

You can add items to a `List` using the `add` method:

```java
List<Integer> luckyNumbers = new ArrayList<>();
luckyNumbers.add(4);
luckyNumbers.add(8);
luckyNumbers.add(15);
luckyNumbers.add(16);
luckyNumbers.add(23);
luckyNumbers.add(42);

// luckyNumbers now holds the data [4, 8, 15, 16, 23, 42]
```

### Getting items out of a List

You can get items out of a list using the `get` method:

```java
// Filling up the list just as above
List<Integer> luckyNumbers = new ArrayList<>();
luckyNumbers.add(4);
luckyNumbers.add(8);
luckyNumbers.add(15);
luckyNumbers.add(16);
luckyNumbers.add(23);
luckyNumbers.add(42);

// Getting numbers out of the list
int four = luckyNumbers.get(0);
int twentyThree = luckyNumbers.get(4);
```

### Inserting items into the middle of a List

You can insert items into the middle of a List using a variant of the `add` method that also accepts an index to insert the item at:

```java
List<Integer> numbers = new ArrayList<>();
numbers.add(1);
numbers.add(2);
numbers.add(3);

// numbers is now [1, 2, 3]

// Insert 4 at the beginning (index 0)
numbers.add(0, 4);
// numbers is now [4, 1, 2, 3]

// Insert 5 in the middle (index 2)
numbers.add(2, 5);
// numbers is now [4, 1, 5, 2, 3]
```

### Iterating over a List

You can iterate over every item in a list in two ways.

Firstly using a plain for-loop:

```java
List<String> words = new ArrayList<>();
words.add("Veni");
words.add("Vidi");
words.add("Vici");

for (int index = 0; index < words.size(); index++) {
    System.out.println(words.get(index));
}
```

This code loops over each index from 0 to the size of the list, and for each index, gets that item from the list and prints it out.

You can also iterate over the items of a list directly without needing to use the index:

```java
List<String> words = new ArrayList<>();
words.add("Veni");
words.add("Vidi");
words.add("Vici");

for (String word : words) {
    System.out.println(word);
}
```

This automatically loops over every `String` kept in `words` and assgns it to a variable called `word`, which is then printed in the body of the loop.

## Map

The `Map` structure in Java acts a bit like a dictionary. Whereas a dictionary contains a set of words and a definition for each word, a `Map` contains a set of _keys_ and a _value_ for each key.

When you look up a word in a dictionary, you can get the definition for that word. Similarly, when you look up a _key_ in a `Map`, you can retrieve the _value_ associated with that key.

### Creating a Map

You can create a `Map` using the following code:

```java
Map<String, Integer> agesOfPeople = new HashMap<>();
```

This creates a `Map` where the keys are of type `String` and the values are of type `Integer`.

### Adding values to a Map

You can add values to a `Map` using the `put` method. The `put` method accepts the key you want to save, and the value that should be associated with it. For example, to store the ages of some people:

```java
Map<String, Integer> agesOfPeople = new HashMap<>();
agesOfPeople.put("Sam", 24);
agesOfPeople.put("Tom", 22);
```

### Getting values out of a Map

You can look up the value associated with a particular key using the `get` method on `Map`:

```java
Map<String, Integer> agesOfPeople = new HashMap<>();
agesOfPeople.put("Sam", 24);
agesOfPeople.put("Tom", 22);

int samsAge = agesOfPeople.get("Sam");
int tomsAge = agesOfPeople.get("Tom");
```

### Iterating over a Map

You can iterate over the keys of a map like this:

```java
Map<String, Integer> myMap;

// ...

for (String key : myMap.keySet()) {
    System.out.println(key + " : " + myMap.get(key));
}
```

This code will loop over all the keys of `myMap` and print out each key along with its associated value.

If you don't care about keys and just want the values, you  can do so using a loop like this:

```java
Map<String, Integer> myMap;

// ...

for (Integer value : myMap.values()) {
    System.out.println(value);
}
```
