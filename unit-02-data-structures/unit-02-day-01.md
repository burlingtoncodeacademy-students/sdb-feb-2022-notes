# Arrays

_Arrays are containers that hold any data type._

## What makes an array an array

- They hold multiple values delineated by a comma.

- Their order is static unless changed by you.

- Accepts duplicate values.

### **Creating an array**

`["apple", "banana", "cherry"]`

- Square brackets are the syntax to create an array.

- Items in the array are separated by commas.

## Array Indexes

- Each item has an index:

  - you can find items by their index number.

  - indexes are 0 based.

### **Accessing the Array by Index**

```js

let fruits = ["apple", "banana", "cherry"]

fruits[1]

//fruits[1] === "banana"

```

Why is `fruits[1]` equal to "banana"? Arrays are 0-indexed.

### **`length` Property**

Using the `.length` property will return the number of objects in the array.

_`.length` is not 0-indexed._

`array[array.length -1]` is how to retrieve the last item in the array.

`array[array.length]` would return `undefined`, as the last item in an array is always an empty value.

## Array Methods

[MDN: Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Methods_2) contains a ton of different properties that work with array values

### **Adding Values to an Array**

`.push` adds a single value to the end of an array

- you can push multiple items at once by putting a comma between your values

### **Yarra Lasrever**

you can use `array.reverse()` to return your array in reverse order

### **Slicing and Dicing**

You can `slice` an array to cut it into smaller arrays.

```js

let fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

let fruits1To3 = fruits.slice(1,3) // slices from item 1 to item 3

let fruits2ToEnd = fruits.slice(2) // slices from item 2 to the end of array

console.log(fruits1To3)
console.log(fruits2ToEnd)

//fruits1to3 === [ 'banana', 'cherry' ]
//fruits2ToEnd === [ 'cherry', 'date', 'elderberry' ]

```

## Manipulating Arrays

### **Adding to the Array**

`[]` is how to add new entries to our array.

```js

let fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

fruits[0] = "kiwi"

console.log(fruits)

//fruits === [ 'kiwi', 'banana', 'cherry', 'date', 'elderberry' ]

```

`fruits[0] = 'apricot'` will set the item in the `[0]` index to the String 'apricot'

### **Arrays into Strings**

There are multiple ways to turn an Array into a String:

#### **`.join()`**

```js
let fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

let joinedFruits = fruits.join()

//joinedFruits === 'apple,banana,cherry,date,elderberry'

```

#### **`.join(" and ")`**

```js

let fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

let joinedAndFruits = fruits.join(" and ")

console.log(joinedAndFruits)

//joinedAndFruits === 'apple and banana and cherry and date and elderberry'

```

#### **`.toString()`**

```js
let fruits = ['apple', 'banana', 'cherry', 'date', 'elderberry']

let stringFruits = fruits.toString()

console.log(stringFruits)

//stringFruits === 'apple,banana,cherry,date,elderberry'

```

### **String to Array**

Turning a string into an array

```js
let dogToArray = "dog".split('')
console.log(dogToArray)

//dogToArray === [ 'd', 'o', 'g' ]
```

### **Looping and Iterating**

> _"Iterating"_ executes a code block once, applying its changes to every value within the array.
> _"Looping"_ executes a code block multiple times until its stop condition is met.

#### **`for` Loop**

This reads as let i = 0, run this loop until i < fruits.length, increment i by 1 every execution.

```js

for(let i=0; i< fruits.length; i++) {

    console.log(fruits[i])

}

```

#### **`for...of` Loop**

This loop will execute the attached block for every item in the array (fruit (value) or fruits (array)).

```js

for(let fruit of fruits){

    console.log("I like " + fruit + "!")

}

```

#### **`.forEach()` Iteration Method**

Similarly, this loop will execute the code block upon every item in the array.

```js

fruits.forEach((fruit)=>{

    console.log("I like " + fruit + "!")

})

```

#### **`.includes` Array Iteration Method**

This iteration method will check the array to see if it includes the given value; it will return true or false.

```js

let fruits = ["apple", "banana", "cherry"]

let containsKiwi = fruits.includes("kiwi")

console.log(containsKiwi)

//containsKiwi === false

```

#### **`.find` Array Iteration Method**

This iteration method will test every value in the array according to its callback function. It will only return the _first_ value that passes the test. It will return `undefined` if no value passes the test.

```js
let fruits = ["apple", "banana", "cherry"]

let findB = fruits.find(fruit => fruit.includes("b"));

console.log(findB);

//containsB === "banana"

```

#### **`.filter` Array Iteration Method**

This iteration method will test every value in the array and return a _new_ array that contains every value that passed the test.

```js
let fruits = ["apple", "banana", "cherry"]

let filterA = fruits.filter(fruit => fruit.includes("a"))

console.log(filterA)

//filterA === [ 'apple', 'banana' ]

```

#### **`.map` Array Iteration Method**

This iteration method will return a _new_ array populated with the results of the function it executes.

```js

let fruits = ["apple", "banana", "cherry"]

let yell= function(word) {

    return word.toUpperCase();

}

let fruitsYelling = fruit.map(yell)

console.log(fruitsYelling)

//fruitsYelling === [ 'APPLE', 'BANANA', 'CHERRY' ]

```

> **Aside: Method Chaining**

- Method chaining takes the **result** from one method, and immediately calls **another** method on it.

```js
let fruits = ["apple", "banana", "cherry"]

let yellFruitsFast = fruits.slice(" ").join("").toUpperCase()

console.log(yellFruitsFast)

//yellFruitsFast === 'APPLEBANANACHERRY'

```

**Further Resources**

- [Eloquent JS Chapter 4](https://eloquentjavascript.net/04_data.html)

- [Array Iteration Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Iteration_methods)
