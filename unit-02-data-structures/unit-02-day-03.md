# Classes & Constructors

## What is a Class and What is a Constructor?

A class defines a type of object and are used to instantiate many objects with similar properties and methods.

While not every class has a constructor, they are necessary to template these properties and methods.

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type
     }

 relax() {
     console.log(`You relax underneath the ${this.age} ${this.type} tree.`)
    }
}

```

Now that we have made our Tree class, let's instantiate a new Tree that we can relax under.

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type
    }

 relax() {
     console.log(`You relax underneath the ${this.age} ${this.type} tree.`)
    }
}

 let appleTree = new Tree("young", "apple")

 appleTree.relax()
 //'You relax underneath the young apple tree.'

```

But there are more trees than this that we can enjoy.

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type  
    }

 relax() {
     console.log(`You relax underneath the ${this.age} ${this.type} tree.`)
    }
}

 let appleTree = new Tree("young", "apple")
 let oakTree = new Tree("old", "oak")
 let palmTree = new Tree("young", "palm")

 appleTree.relax()
 //'You relax underneath the young apple tree.'

 oakTree.relax()
 //'You relax underneath the old oak tree.'

 palmTree.relax()
 //'You relax underneath the young palm tree.'

```

### **Error Handling: Default Values**

What if a value isn't passed to our constructor?

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type  
    }

 relax() {
     console.log(`You relax underneath the ${this.age} ${this.type} tree.`)
    }
}

 let youngTree = new Tree("young")

 youngTree.relax()
 //'You relax underneath the young undefined tree.'

```

What happened? Every property created in the constructor correlates to the order the values are passed in when we create a new Object. While the constructor did receive `this.age`, it did not receive `this.type` and thus returned `undefined`.

But, we can set default values in our constructor to prevent this from occurring.

We do this utilizing the logical OR `||`; this tells our constructor to use the value passed to it OR, if there is no passed value, "beautiful".

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type || "beautiful"  
    }

 relax() {
     console.log(`You relax underneath the ${this.age} ${this.type} tree.`)
    }
}

 let youngTree = new Tree("young")

 youngTree.relax()
 //'You relax underneath the young beautiful tree.'

```

### **Error Handling: Throw an Error**

We can plan for values to not be input, but what if we want to let the user know that they did not include any input or they input the wrong information?

We can create an `if` conditional statement that will `throw` a message.

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type  
    }

 relax() {

     if (this.age === undefined || this.type === undefined)
     throw "Hey! You forgot to describe your tree!"
    }
}

 let youngTree = new Tree("young")

 youngTree.relax()
 //'Error: Hey! You forgot to describe your tree!'

```

We can also inform the user of an error via a console log, which can be a more appealing user experience dependent upon the intention of your software. Are you alerting a fellow developer to an issue, or a non-technical user?

```js
class Tree {
    constructor(age, type) {
      this.age = age
      this.type = type  
    }


 relax() {

     if (this.age === undefined || this.type === undefined) {
     console.log("Hey! You forgot to describe your tree!")
        }
    }
}

 let youngTree = new Tree("young")

 youngTree.relax()
 //'Hey! You forgot to describe your tree!'

```

# Object Lookup Tables & State Machines

## Lookup Table

A lookup table is an object that is used to map strings to other values.

The search is used as a key in the object, and the result for that search term is the corresponding value.

```js

class Flower {
    constructor(name, color) {
        this.name = name
        this.color = color
    }
}

let tullip = new Flower("tullip","yellow")
let daisy = new Flower("daisy","white")
let rose = new Flower("rose","red")
let lily = new Flower("lily","orange")


let flowerLookUp = {
    "tullip": tullip,
    "daisy": daisy,
    "rose": rose,
    "lily": lily
}


function chooseFlower (flower)  {
    console.log(`You chose a beautiful ${flowerLookUp[flower].color} ${flowerLookUp[flower].name}!`)
}

chooseFlower("tullip")
//'You chose a beautiful yellow tullip!'

```

### **Chaining Notation**

You may have noticed in the previous code example, we had to chain bracket and dot notation in order to access the value that we wanted.

This notation chains similarly to how we have chained methods earlier in the course.

Let's break down `flowerLookUp[flower].color`:

First, `flowerLookUp[flower]` accesses our lookup table at the argument passed to the function. In this case, "tullip".

At this point, our code is `tullip.color`. The `color` property on tullip is "yellow".

This is how we go from:

`'You chose a beautiful ${flowerLookUp[flower].color} ${flowerLookUp[flower].name}!'`

to

 `'You chose a beautiful yellow tullip!'`.

# State and Machines

State describes the status of the entire program or an individual object. It could be text, a number, a boolean, or another data type. You can use it for coordinating code. Once you update state, a bunch of different things can instantly react to that change.

## State Machines

State Machines are transitional mechanisms that allow you to move from one state to the next.

How could we represent a house with a state machine?

```js

let houseMachine = {    

  "door": ["mud room"], 

  "mud room": ["kitchen", "living room"],   

  "kitchen": ["mud room", "living room"],    

  "living room": ["mud room", "kitchen", "bathroom"], 

  "bathroom": ["living room"] 

}

let currentRoom = "door"; 

function changeRoom(newRoom) {    

  if (houseMachine[currentRoom].includes(newRoom)) {   

    currentRoom = newRoom;  

    console.log(`You are now in the ${newRoom}.`) 

  } else {

    console.log("You can't walk through walls...")

  }

}

changeRoom("mud room")
// 'You are now in the mud room.'
changeRoom("bathroom")
//"You can't walk through walls..."

```

As you can see, our state machine will allow you to enter the mud room from the door, but not the bathroom. These are representative of allowable and NOT allowable transitions that our state machine handles for us.

## Further Resources

- [MDN: Object Oriented JS for Beginners](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_JS)

- [Why Do We Care About State?](https://dev.to/reedbarger/what-is-state-and-why-should-we-care-about-it-4o95)
