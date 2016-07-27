# JavaScript Reference

## Variables

You use variables as symbolic names for values in your application. The names of variables, called _identifiers_, conform to certain rules.

A JavaScript identifier must start with a letter, underscore (_), or dollar sign ($); subsequent characters can also be digits (0-9). Because JavaScript is case sensitive, letters include the characters "A" through "Z" (uppercase) and the characters "a" through "z" (lowercase).

### Declaring variables

You can declare a variable in two ways:

With the keyword `var`. For example, `var x = 42`. This syntax can be used to declare both local and global variables.

By simply assigning it a value. For example, `x = 42`. This always declares a global variable and cannot be changed at the local level. **You shouldn't declare variables this way.**

#### Keywords
JavaScript uses words that are special to the language. These words are also referred to as reserved words, which means you cannot use these for your own variables.

Some example keywords include:

- `var`
- `if`
- `else`
- `break`
- `for`
- `while`
- `function`
- `return`

### Evaluating variables

A variable declared using the var statement with no initial value specified has the value `undefined`.

```javascript
var a;
console.log("The value of a is " + a); // logs "The value of a is undefined"
console.log("The value of b is " + b); // throws ReferenceError exception
```

## Primitive Data Types

In JavaScript there are 5 primitive data types. A **primitive** data type is data that is not an `Object` and does not have any methods.

Data Type | Example
--------- | ----------------------
boolean   | true
null      | null
undefined | undefined
number    | 42
string    | "Alice"

### Boolean type

The Boolean data type can only have two possible values: `true` or `false`.

### Null type

The Null type has exactly one value: `null`.

The value `null` is a JavaScript literal representing null or an "empty" value, i.e. no object value is present.

### Undefined type

A variable that has not been assigned a value has the value `undefined`.

### Number type

You can do normal math operations with these data types.

#### Constants

In computer programming, a constant is an identifier whose associated value cannot typically be changed.

`Math` global object has properties for mathematical constants.

Constant       | Value
-------------- | ------------------
`Math.E`       | 2.718281828459045
`Math.LN2`     | 0.6931471805599453
`Math.LN10`    | 2.302585092994046
`Math.LOG2E`   | 1.4426950408889634
`Math.LOG10E`  | 0.4342944819032518
`Math.PI`      | 3.141592653589793
`Math.SQRT1_2` | 0.7071067811865476
`Math.SQRT2`   | 1.4142135623730951

### String type
A sequence of characters used to represent textual data.

     'string text'
     "string text"
     "中文 español English हिन्दी العربية português বাংলা русский 日本語 ਪੰਜਾਬੀ 한국어"

Beside regular, printable characters, special characters can be encoded using escape notation:

Code   | Output
------ | -----------------
\0     | the NUL character
\'     | single quote
\"     | double quote
\\     | backslash
\n     | new line
\r     | carriage return
\v     | vertical tab
\t     | tab
\b     | backspace
\f     | form feed
\uXXXX | unicode codepoint
\xXX   | the Latin-1 character

## Objects
In computer science, an object is a value in memory which is possibly referenced by an identifier.

### Properties
In JavaScript, objects can be seen as a collection of properties.

With the object literal syntax, a limited set of properties are initialized; then properties can be added and removed. Property values can be values of any type, including other objects, which enables building complex data structures. Properties are are identified using key values. A key value is usually represented by a String value.

```javascript
var person = {
  "name": "Bob",
  "age": 37
};

person.name    // "Bob"
person.age     // 37
```

## Arrays
An array literal is a list of zero or more expressions, each of which represents an array element, enclosed in square brackets (`[]`). When you create an array using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified.

```javascript
var animals = ["Dog", "Cat", "Rabbit", "Lion", "Frog"];

animals.length // 5
```

In JavaScript (and many other programming languages) arrays are zero-indexed. This means that the first element of an array is at index `0`, and the last element of the array has index `n-1` where `n` is equal to the length of the array.

```javascript
var fruits = ["Kiwi", "Apple", "Lemon", "Grape", "Strawberry"];

fruits[0]                 // "Kiwi"
fruits[1]                 // "Apple"
fruits[fruits.length - 1] // "Strawberry"
```

## Expressions
An expression is any valid unit of code that resolves to a value.

The code `3 + 4` is an example of the second expression type. This expression uses the `+` operator to add three and four together without assigning the result, seven, to a variable.

The expression `x = 7` is an example of the first type. This expression uses the = operator to assign the value seven to the variable `x`. The expression itself evaluates to seven.

Expressions can be combined, so `x = 3 + 4` first evaluates the expression `3 + 4` to the value seven. Then, the expression `x = 7` is evaluated so that the value of `x` is seven.

JavaScript has the following expression categories:

- Arithmetic: evaluates to a number, for example `3.14159`.
- String: evaluates to a character string, for example, `"Fred"` or `"234"`.
- Logical: evaluates to `true` or `false`.
- Object: evaluates to an object.


## Operators

JavaScript has both _binary_ and _unary_ operators, and one special ternary operator, the conditional operator.

A binary operator requires **two** operands, one before the operator and one after the operator:

- `3 + 4`
- `x * y`

A unary operator requires a single operand, either before or after the operator:

- `x++`
- `--y`

### Arithmetic operators

Arithmetic operators take numerical values (either literals or variables) as their operands and return a single numerical value.

Operator   | Description                  | Example  | Result
---------- | ---------------------------- | -------- | ------------------
`+`        | Addition                     | 7 + 1    | 8
`-`        | Subtraction                  | 4 - 9    | -5
`*`        | Multiplication               | 6 * 8    | 48
`/`        | Division                     | 10 / 3   | 3.3333333333333335
`%`        | Modulus (division remainder) | 5 % 2    | 1

Use this value for the table below: `var x = 5;`

Operator   | Description                  | Example  | Result
---------- | ---------------------------- | -------- | ------------------
`-`        | Negation                     | -x       | -5
`++`       | Increment                    | x++      | 5
`--`       | Decrement                    | x--      | 4

### Comparison operators

A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values.

In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically.

Use these values for the table below:

```javascript
var x = 3,
    y = 4;
```

Operator | Name                       | Description                                                                       | Examples returning true
-------- | -------------------------- | --------------------------------------------------------------------------------- | -----------------------
`==`     | Equal                      | Returns `true` if the operands are equal.                                         | `x == 3`, `x == "3"`, `3 == "3"`
`!=`     | Not equal                  | Returns `true` if the operands are not equal.                                     | `x != 4`, `y != "3"`
`===`    | Strict equal               | Returns `true` if the operands are equal and of the same type.                    | `3 === x`
`!==`    | Strict not equal           | Returns `true` if the operands are not equal and/or not of the same type.         | `x !== "3"`
`>`      | Greater than               | Returns `true` if the left operand is greater than the right operand.             | `y > x`
`>=`     | Greater than or equal      | Returns `true` if the left operand is greater than or equal to the right operand. | `x >= 3`, `y >= x`
`<`      | Less than                  | Returns `true` if the left operand is less than the right operand.                | `x < y`
`<=`     | Less than or equal         | Returns `true` if the left operand is less than or equal to the right operand.    | `y <= 5`, `x <= y`

### Logical operators

Logical operators are typically used with Boolean (logical) values; when they are, they return a Boolean value. However, the && and || operators actually return the value of one of the specified operands, so if these operators are used with non-Boolean values, they may return a non-Boolean value.

Operator   | Name        | Usage              | Description
---------- | ----------- | ------------------ | -----------
`&&`       | Logical AND | `expr1 && expr2`   | Returns `expr1` if it can be converted to `false`; otherwise, returns `expr2`. Thus, when used with Boolean values, `&&` returns `true` if both operands are `true`; otherwise, returns `false`.
<code>&#124;&#124;</code>     | Logical OR  | <code>expr1 &#124;&#124; expr2</code> | Returns `expr1` if it can be converted to `true`; otherwise, returns `expr2`. Thus, when used with Boolean values, <code>&#124;&#124;</code> returns `true` if either operand is `true`; if both are `false`, returns `false`.
`!`        | Logical NOT | `!expr`            | Returns `false` if its single operand can be converted to `true`; otherwise, returns `true`.

### String operators

In addition to the comparison operators, which can be used on string values, the concatenation operator (+) concatenates two string values together, returning another string that is the union of the two operand strings. For example, `"my " + "string"` returns the string `"my string"`.

### Assignment operators

An assignment operator assigns a value to its left operand based on the value of its right operand. The basic assignment operator is equal (`=`), which assigns the value of its right operand to its left operand. That is, `x = y` assigns the value of `y` to `x`.

The other assignment operators are shorthand for the operations listed in the following table:

Shorthand operator   | Meaning
-------------------- | -----------
`x += y`             | `x = x + y`
`x -= y`             | `x = x - y`
`x *= y`             | `x = x * y`
`x /= y`             | `x = x / y`
`x %= y`             | `x = x % y`

### Conditional operator

The conditional operator is the only JavaScript operator that takes three operands. The operator can have one of two values based on a condition. The syntax is:

```javascript
condition ? val1 : val2
```

For example,

```javascript
var status = (age >= 18) ? "adult" : "minor";
```
This statement assigns the value "adult" to the variable status if age is eighteen or more. Otherwise, it assigns the value "minor" to status.

## Statements (Control Flow)
JavaScript supports a compact set of statements, specifically control flow statements.

### Block Statements

A block statement is used to group statements. The block is delimited by a pair of curly brackets:

```javascript
{
  statement_1;
  statement_2;
  .
  .
  .
  statement_n;
}
```

Block statements are commonly used with control flow statements (e.g. `if`, `for`, `while`).

```javascript
while (x < 10) {
  x++;
}
```

```javascript
if (y == 10) {
  y += 5;
}
```

### Conditional Statements

A conditional statement is a set of commands that executes if a specified condition is `true`. JavaScript supports two conditional statements: `if...else` and `switch`.

#### `if...else` Statement

Use the `if` statement to execute a statement if a logical condition is `true`. Use the optional `else` clause to execute a statement if the condition is `false`. An `if` statement looks as follows:

```javascript
if (condition) {
  statement_1;
}
else {
  statement_2;
}
```

You may also compound the statements using `else if` to have multiple conditions tested in sequence, as follows:

```javascript
if (condition_1) {
  statement_1;
}
else if (condition_2) {
  statement_2;
}
else if (condition_n) {
  statement_n;
}
else {
  statement_last;
}
```

#### `switch` Statement

A `switch` statement allows a program to evaluate an expression and attempt to match the expression's value to a case label. If a match is found, the program executes the associated statement. A switch statement looks as follows:

```javascript
switch (expression) {
  case label_1:
    statements_1
    [break;]
  case label_2:
    statements_2
    [break;]
  ...
  default:
    statements_def
    [break;]
}
```

The program first looks for a `case` clause with a label matching the value of expression and then transfers control to that clause, executing the associated statements. If no matching label is found, the program looks for the optional `default` clause, and if found, transfers control to that clause, executing the associated statements. If no `default` clause is found, the program continues execution at the statement following the end of `switch`. By convention, the `default` clause is the last clause, but it does not need to be so.

The optional `break` statement associated with each `case` clause ensures that the program breaks out of `switch` once the matched statement is executed and continues execution at the statement following switch. If `break` is omitted, the program continues execution at the next statement in the `switch` statement.

**Example**

In the following example, if `dayOfTheWeek` evaluates to `"Monday"`, the program matches the value with case `"Monday"` and executes the associated statement. When `break` is encountered, the program terminates `switch` and executes the statement following `switch`. If `break` were omitted, the statement for case `"Tuesday"` would also be executed.

```javascript
switch (dayOfTheWeek) {
  case "Monday":
    console.log("Fun Day!");
    break;
  case "Tueday":
    console.log("Cruise Day!");
    break;
  case "Wednesday":
    console.log("Friends Day!");
    break;
  default:
    console.log("Sorry, I ran out of rhymes.");
}
console.log("What's next?");
```

### Loop Statements

A loop is a set of commands that executes repeatedly until a specified condition is met. JavaScript supports the `for`, `do while`, and `while` loop statements.

#### `for` Statement

A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop. A for statement looks as follows:

```javascript
for ([initialExpression]; [condition]; [incrementExpression])
   statement
```

When a for loop executes, the following occurs:

  1. The initializing expression `initialExpression`, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression  can also declare variables.
  2. The `condition` expression is evaluated. If the value of `condition` is `true`, the loop statements execute. If the value of `condition` is false, the for loop terminates. If the `condition` expression is omitted entirely, the `condition` is assumed to be true.
  3. The `statement` executes. To execute multiple statements, use a block statement (`{ ... }`) to group those statements.
  4. The update expression `incrementExpression`, if there is one, executes, and control returns to step 2.

**Example**

```javascript
for (var i = 0; i < 5; i++) {
  console.log(i);
}
```

**Output**

    0
    1
    2
    3
    4

#### `do...while` Statement

The `do...while` statement repeats until a specified condition evaluates to false. A `do...while` statement looks as follows:

```javascript
do {
   statement
} while (condition);
```

`statement` executes once before the condition is checked. To execute multiple statements, use a block statement (`{ ... }`) to group those statements. If `condition` is true, the statement executes again. At the end of every execution, the condition is checked. When the condition is false, execution stops and control passes to the statement following `do...while`.

#### `while` Statement

A `while` statement executes its statements as long as a specified condition evaluates to true. A `while` statement looks as follows:

```javascript
while (condition) {
  statement
}
```

The condition test occurs _before_ statement in the loop are executed. If the `condition` returns true, `statement` is executed and the condition is tested again. If the condition returns false, execution stops and control is passed to the statement following `while`.


## Functions
Generally speaking, a function is a "subprogram" that can be called by code external (or internal in the case of recursion) to the function. Like the program itself, a function is composed of a sequence of statements called the function body. Values can be passed to a function, and the function can return a value.

```javascript
/* Declare the function 'myFunc' */
function myFunc(theObject) {
  theObject.brand = "Toyota";
}

/*
 * Declare variable 'mycar';
 * create and initialize a new Object;
 * assign reference to it to 'mycar'
 */
var mycar = {
  brand: "Honda",
  model: "Accord",
  year: 1998
};

/* Logs 'Honda' */
console.log(mycar.brand);

/* Pass object reference to the function */
myFunc(mycar);

/*
 * Logs 'Toyota' as the value of the 'brand' property
 * of the object, as changed to by the function.
 */
console.log(mycar.brand);
```

To return a specific value other than the default, a function must have a `return` statement that specifies the value to return. A function without a return statement will return a default value. In the case of a `constructor` called with the `new` keyword, the default value is the value of its `this` parameter. For all other functions, the default return value is `undefined`.

The parameters of a function call are the function's arguments. Arguments are passed to functions by value. If the function changes the value of an argument, this change is not reflected globally or in the calling function. However, object references are values, too, and they are special: if the function changes the referred object's properties, that change is visible outside the function, as shown in the following example:

In JavaScript, functions are first-class objects, i.e. they are objects and can be manipulated and passed around just like any other object. Specifically, they are `Function` objects.

### Constructor functions

Alternatively to creating objects with the literal notation, you can also create objects using constructor functions.

  1. Define the object type by writing a constructor function. (Usually the first letter of the function name is capitalized.)
  2. Create an instance of the object with new.

To define an object type, create a function for the object type that specifies its name, properties, and methods. For example, suppose you want to create an object type for cars. You want this type of object to be called `car`, and you want it to have properties for make, model, and year. To do this, you would write the following function:

```javascript
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
```


## Exception Handling Statements

You can throw exceptions using the throw statement and handle them using the `try...catch` statements.

### `throw` Statement

Use the `throw` statement to throw an exception. When you throw an exception, you specify the expression containing the value to be thrown:

```javascript
throw expression;
```

You may throw any expression, not just expressions of a specific type. The following code throws several exceptions of varying types:

```javascript
throw "Error2";   //String type
throw 42;         //Number type
throw true;       //Boolean type
throw { toString: function() { return "I'm an object!"; } };
```

Notice the use of `this` to assign values to the object's properties based on the values passed to the function.

Now you can create an object called `mycar` as follows:

```javascript
var mycar = new Car("Eagle", "Talon TSi", 1993);
```
This statement creates mycar and assigns it the specified values for its properties. Then the value of `mycar.make` is the string `"Eagle"`, `mycar.year` is the integer `1993`, and so on.

You can create any number of car objects by calls to new. For example,

```javascript
var kenscar = new Car("Nissan", "300ZX", 1992);
var vpgscar = new Car("Mazda", "Miata", 1990);
```

### `try...catch` Statement

The `try...catch` statement marks a block of statements to try, and specifies one or more responses should an exception be thrown. If an exception is thrown, the `try...catch` statement catches it.

The `try...catch` statement consists of a `try` block, which contains one or more statements, and zero or more `catch `blocks, containing statements that specify what to do if an exception is thrown in the `try` block. That is, you want the `try` block to succeed, and if it does not succeed, you want control to pass to the `catch` block. If any statement within the `try` block (or in a function called from within the `try` block) throws an exception, control immediately shifts to the `catch` block. If no exception is thrown in the `try` block, the `catch` block is skipped. The `finally` block executes after the `try` and `catch` blocks execute but before the statements following the `try...catch` statement.

```javascript
try {
  // generates an exception
  throw "myException"
}
catch (error) {
  // statements to handle any exceptions
}
```

### The `finally` Block

The `finally` block contains statements to execute after the `try` and `catch` blocks execute but before the statements following the `try...catch` statement. The `finally` block executes whether or not an exception is thrown. If an exception is thrown, the statements in the `finally` block execute even if no `catch` block handles the exception.

```javascript
openMyFile();
try {
  writeMyFile(theData); //This may throw a error
}
catch(error) {
  handleError(error); // If we got a error we handle it
}
finally {
    closeMyFile(); // always close the resource
}
```

## Comments

Comments are author notations that explain what a script does. Comments are ignored by the interpreter. JavaScript supports Java and C++-style comments:

- Comments on a single line are preceded by a double-slash (//).
- Comments that span multiple lines are preceded by /* and followed by */:

**Example**

The following example shows two comments:

```javascript
// This is a single-line comment.

/* This is a multiple-line comment. It can be of any length, and
you can put whatever you want here. */
```
