# Objects

_Objects are representations of things._

Programmers are writing code to represent real things. Objects translate real world to data and are written in object literal syntax.

Information is stored in a `key: value` pair within the Object. In our Object below, `name: Phife` has the  `key` of "name", and a `value` of "Phife". The `key` is used to access the `value`.

```js
let dog = {

name: 'Phife',

color: 'liver and white',

age: '15 months',

breed: 'Brittany'

}
```

## Accessing the Object

### Dot Notation

Dot notation is one option for accessing information within the object.

```js
let dog = {

name: 'Phife',

color: 'liver and white',

age: '15 months',

breed: 'Brittany',

}

console.log(dog.name) //=> 'Phife'

```

### Bracket Notation

Bracket notation is another option for accessing information within the object.

```js
let dog = {

name: 'Phife',

color: 'liver and white',

age: '15 months',

breed: 'Brittany',

}

console.log(dog["breed"] //=> 'Brittany'

```

### Dot or Bracket Notation?

Dot notation requires less characters, while bracket notations tends to be more flexible in terms of what argument it will take.

### **Adding `key: value` Pairs to an Object**

You can utilize either dot or bracket notation and an assignment operator to add more `key: value` pairs to your Object.

```js
let dog = {

name: 'Phife',

color: 'liver and white',

age: '15 months',

breed: 'Brittany',

}

dog.gender = "boy"
dog["dad"] = "Matt"

console.log(dog)

/* {
  name: 'Phife',
  color: 'liver and white',
  age: '15 months',
  breed: 'Brittany',
  gender: 'boy',
  dad: 'Matt'
}
*/

```

### **`Object.keys()`**

You may not always know all of the keys an object has. With the `Object.keys()` method, you can learn them.

```js
let dog = {

name: 'Phife',

color: 'liver and white',

age: '15 months',

breed: 'Brittany',

}


console.log(Object.keys(dog)) //=> [ 'name', 'color', 'age', 'breed' ]


```

## Object Methods

A method is a function attached to an object as a property and as JS is a dynamic language, you can add methods to any object.

To create a method, the `key` is the name of the method and the `value` is the function you want to execute.

### **Creating An Object With a Method**

```js
let dog = {

name: 'Phife',

color: 'liver and white',

age: '15 months',

breed: 'Brittany',

bark: function() {

    console.log("BARK BARK!")

    }

}

dog.bark() // => "BARK BARK!"


```

## **Further Reading**

- [MDN JavaScript Object Basics](<https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics>)
- [Modern JavaScript Object Methods](<https://javascript.info/object-methods>)
