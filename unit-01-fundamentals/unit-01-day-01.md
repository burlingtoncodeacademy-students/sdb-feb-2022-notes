# Unit-1 Day-1

## Introduction

### What is code?

- General
  - Coding/programming is creative and human.
  - The computer does not read what you write in VSCode, it is translated into language the computer can understand.
- In Computers
  - A series of instructions that tells a computer what to do
  - Computers are very fast, but very stupid. They will only follow your instructions, which can cause error.

### What is coding NOT?

- Coding is **not** identical to mathematics
  - some logic (if/then/and/or/ect)
  - Mostly just counting ("do this 10 times")

- Coding is **not** solitary
  - code usually happens in teams

- Coding is **not** about finding the right answer
  - There are always more then one way to do it
  - There are tradeoffs to each solution
  - The hardest part of coding is *defining* the problem, not solving it

### Programmatic Thinking

- What is programmatic thinking?
  - Computers only do exactly what you tell them, they are LITERAL.
  - Errors give you feedback on your progress. New errors mean further progress!

- How can I maximize my learning?
  - Your ability to learn and understand technical material diminishes after about two hours. Take breaks!

### Languages

- Every program is written in a **Language**
  - like Java, Python, or C
  - HTML and CSS and SQL are languages
- computer languages are very specific
- different languages are useful in different areas
- We will be covering JavaScript, HTML, and CSS in this course
  - JavaScript is a very powerful language for web based programming

### What will we learn?

- The command line
  - CLI (Command line interface) aka Terminal
- Strings, Arrays, Variables, Objects, Loops, Files
- Run code interactively (in your CLI) or from a file
- Make a simple website to run on your computer
- Push your websites to the internet and make them Live

### What if I know this already?

- Pair up
- Review is helpful
- Help your partner, or neighbor
- You will understand it better through teaching it, utilize breakout rooms!

### Further Resources

- [MDN (Mozilla Development Network)](https://developer.mozilla.org/en-US/)
  - Official documentation on JavaScript.

- [Eloquent Javascript](https://eloquentjavascript.net/)
  - Open source book for further reading.

- Community Curated Websites
  - Stack Overflow
  - CSS-tricks.com
  - Medium.com
  - Dev.to
  - Web.dev

### Errors are your computer trying to work with you

- Full file path: the exact file where the error occurred.
- Line number: the exact line where the error occurred.
- Error type: the type of error.
- Stack trace: the activity the application was in the middle of when the error occurred.

### The Command Line

- How we talk directly to the computer
- You can issue **commands** to the computer
- the CLI is different then a GUI (Graphical User Interface)
  - a CLI is more primitive **and more powerful**

### Directories

- a *directory* is a location on your hard disk
  - also called a *folder*
- directories can contain *files*
  - they can also contain other directories
    - aka sub directories

### Where am I?

- while inside terminal you're always "inside" a directory.
- you can type `pwd` and hit return.
  - this prints your file path at your current location

### Home Directory

- If you store your files in your home directory, things will get cluttered.
- For this class we recommend:
  - create a `code` directory inside of your home directory.
  - create a new directory inside of `code` for each lesson or project.
    - or you can create a `lessons` directory and a `projects` directory inside of your `code` directory

### The Path

- The command line is *entirely* dependant on the file path. You can only run files from their correct location in the directory.

- `.` this directory im inside of
- `..` the directory that contains this directory
- `/another-directory` means "look for a directory named 'another-directory"
- `/another-directory/further-down` allows you to chain directories
- hitting `Tab` while `cd`ing will autofill directory names.

### Listing Directory Contents

- you can type `ls` and it will show the entire contents of the current directory

- you can also type `ls -al` this shows all *hidden* files as well as everything that `ls` would show you

### Making a Directory

- you can use `mkdir` ("make directory") and it creates a new subdirectory

`mkdir code`

this will create your "code" sub directory

### Changing Directories

- `cd` ("change directory") moves you into the directory

- `cd code` will move you into your `code` directory

### Your Code File

- `code .` open VSCode from this directory
- `touch example.js` creates a new file in this directory, requires the name of the file and the extension of the file type

### Basic Command Review

- `pwd` - shows the name of the current directory
- `ls` - shows the contents of the current directory
- `mkdir` - creates a sub directory inside of the current directory
- `cd` - moves into a different directory

> both `mkdir` and `cd` take a second word after for the directory they are referring to

- `ctrl + l` - clears the content of your terminal
- `code .` - opens VS Code from within the directory your Terminal is currently located in
- `ctrl + c` - kills whatever is currently happening in your terminal. tap twice to confirm ending the process.
- `UP and DOWN arrow keys` cycle through previous commands in Terminal

### LAB: Hello World

- console.log("") prints to the console
- `node example.js` typed into the command line, runs our file in a Node environment

### Recommended VS Extensions

- Bracket Pair Colorizer - distinguishes bracket pairs by color
- Prettier Code Formatter - differently opinionated code formatting
- Live Server - local development server you will need in a couple weeks
- Code Spell Checker - as described
- Highlight Matching Tag - highlights matching closing and opening tags
- indent-rainbow - colorizes code tab indentation

### Let's code

### Values

- A **Value** is a location in computer memory that stores DATA
- There are many types of values
  - Number
  - Strings
  - Booleans
  - Null
  - Symbol
- Different kinds of values are called **types**

### Numbers

- A **Number** is exactly what it sounds like, any integer or decimal.

- There is a Math class specific to mathematical/numerical operations.
  - Some methods off of the Math class include:
            - Math.round() rounds to the nearest integer
            - Math.floor() returns the largest integer less than or equal to a given number
            - Math.random() provides a random integer

- Off by One Errors
  - Computers start counting at 0; humans start at 1.
  - The fix is easy, add or subtract 1 to the value!

### Strings

- Any amount of characters between two quotation marks, single or double, is a **String**. Including integers.
  - 42 is a Number primitive type. "42" is a String primitive type. '42' is a String primitive type.

- Methods that can be used on strings include:
        - "example".slice(2, 4) will return "am". This means from index of character 2 to character 4.
            - "example".slice(2) will return "ample". This means from index of character 2 to the end of the string.
        - string.length will return the length of the string.

### Booleans

- 'True' and 'false' are the only two **Boolean** values.
  - Every value in Javascript can be coerced into a Boolean upon evaluation.

### Null

- **Null** is a nonexistent value.
- **Undefined** is an "I don't know" value.
- **NaN** is a "Not a number" value.

### BigInt

- Special handling for large numbers; not relevant to this course.

### Symbols

- Not an operator, introduced to allow for weak encapsulation. Not relevant to this course.

## Operators

- `>`, `+`, `-`, `.`, `=`, `===` are all operators. You can think of these as shorthand for specific, prebuilt functions.
  - Types include:
    - Assignment
    - Comparison
    - Arithmetic
    - Logical
    - Conditional
- Operators have precedence and associativity. Precedence determines in which order operators execute, associativity determines which direction same precedence operators will execute. See MDN's "Operator Precedence" page for more in-depth.

### Comments

- `//` putting two slashes in a row indicates that this is a comment, meaning a note written by the programmer to communicate what the code is doing.
- `/* example */` allows you to write an inline OR multi-line comment.
- Highlight your code and press `CTRL-/` to comment out code in VSCode.

### Type Coercion

- Javascript is 'dynamically' typed. This means that because Javascript always wants to evaluate down to a single value, it will decide the type of a value in mixed operations.
        - 4  + "2" will evaluate to "42". Javascript coerced the Number 4 into the String 4 in order to evaluate to a single value.

### Type Conversion

- As opposed to **COERCION**, we can tell Javascript explicitly to convert value types. One such method would be calling `30.toString()` where the Number 30 becomes the String '30'.

### Expressions vs Statements

- An expression is code that **EVALUATES**. A mathematical equation is an expression.
- A statement is code that **EXECUTES**, and frequently contains expressions. Statements end with a semi-colon.
- Types of statements:
        Logical blocks
        Functions
        Loops

### QA

- Q: Do I need a new SSH key if I switch to a new computer?
  - A: Yes SSH keys are bound to specific machines. You can have multiple on your GitHub account.

- Q: How do I Google an error message?
  - A: Put your operating system, the application (if it occurred in one), and the error message exactly as given.

- Q: Can I execute a file in a Node environment in my command line?
  - A: No. When you are in Node, it creates its own process environment in order to execute code.

- Q: What happens if I slice at a negative number? For example, "apple".slice(-1)
  - A: Slicing from a negative number will go backwards from the end of the string. In this case, the return would be "e".

- Q: Should I expect a value returned in VSCode?
  - A: No. While your terminal in Node is an active execution environment, VSCode is not. You will have to execute your file in the terminal (outside of the Node environment) using `node filename.js`.
