# Unit-1 Day-2

## Functions

Functions are "self contained" modules of code that accomplish a specific task. Functions usually "take in" data, process it, and "return" a result. Once a function is written, it can be used over and over and over again. Functions can be "called" from the inside of other functions.

They are named just like variables, but make sure they are concise.

You can call a function by using it's name plus `()` -`function add(numOne, numTwo)` would be called by using `add()`

### Passing Variables to Functions

When you pass a variable to a function, that variable's value is assigned to a parameter.

### The Four Functional Syntaxes

1. Function Declaration syntax - the most common - `function variable(x) {Do stuff}`
2. Function Expression - `let variable = function(x){Do stuff}`
3. Arrow Function Expression - `let variable = (x) => {Do Stuff}`
4. Arrow Function Expression w/ Implicit Return Value - `let variable = (x) => Stuff`

Outside of the functional declaration, the other functions "name" is the variable it points to

## Null

### Null is Useful

Null is a **falsy** value that means there is no value
Null can be used as a place holder, or a 'nothing yet' scenario, and as a guard clause in your program

### Null Errors are good

Errors tell us:

- There is a mistake somewhere,
- What ths mistake is,
- and often how to fix it.

### TypeError explained

"TypeError" is an error about data types.
"Cannot read property" means there is no such property
"of null" is the value you were using
This error is confusing because the reason and location of the error is at the end of the message

### Null Pointer Errors

Very Common Error
The trick is reading the error to determine:

1. Where (which line)
2. Which variable is null
3. Why it was null

### Nulls are falsy

-`null` means nothing, -`undefined` means "I don't know" -`NaN` means Not a Number -`''` means an empty string

### Truthiness

- computers have either a _true_ or _false_ there is no grey area

### Comparisons

```txt
Operator Comparison

<           less than
>           greater than
<=          less than or equal to
>=          greater than or equal to
==          equal to
!=          not equal
===         really equal to
!==         really not equal to

```

We can use these operators to create a true or false statement that can be used to conditionally render code.

### Conditions

- in JS we write conditionals with `if` statements
  - `if(/*argument*/) {/*run this code*/}`

### What is falsyness?

- `false`, `null`, `undefined`, `0`, `NaN`, and an empty string (`""`) are all falsy
- `true` is truthy `false` is falsy

- Be careful though the string `"false"` and the string `"0"` are truthy
  - this is because a string containing any character is truthy even if that character is falsy

### The Tragedy of the Equal Sign

- A single equals sign means **assignment**
  - name = "Alice" -- means "the value of name is "Alice"
- Two or 3 Equal signs means **comparison**
  - name == "Alice" - this is checking to see if the calue of name is "Alice"

### if.. then.. else

- `else` allows **branching**

```js
if (age >= 18) {
  console.log("allowed");
} else{
  console.log("denied");
}
```

- this allows the program to choose one path or the other
  - **if** the first path is not true, it will send the program down the `else` path

### Conjunction Junction

You can combine comparisons with logical Operators

- AND - &&
- OR - ||
- NOT - !

for example:

```js
if (age >= 18 || hasPermissionSlip()) {
    console.log("allowed");
}
```
