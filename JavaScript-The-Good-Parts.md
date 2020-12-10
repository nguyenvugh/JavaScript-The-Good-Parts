# JavaScript-The-Good-Parts

##### Chapter 1.Good Parts
##### Section 1.1. Why JavaScript?
##### Section 1.2. Analyzing JavaScript
##### Section 1.3. A Simple Testing Ground
##### Chapter 2. Grammar
##### Section 2.1. Whitespace
##### Section 2.2. Names
##### Section 2.3. Numbers
##### Section 2.4. Strings
##### Section 2.5. Statements
##### Section 2.6. Expressions
##### Section 2.7. Literals
##### Section 2.8. Functions
##### Chapter 3. Objects
##### Section 3.1. Object Literals
##### Section 3.2. Retrieval
##### Section 3.3. Update
##### Section 3.4. Reference
##### Section 3.5. Prototype
##### Section 3.6. Reflection
##### Section 3.7. Enumeration
##### Section 3.8. Delete
##### Section 3.9. Global Abatement
##### Chapter 4. Functions
##### Section 4.1. Function Objects
##### Section 4.2. Function Literal
##### Section 4.3. Invocation
##### Section 4.4. Arguments
##### Section 4.5. Return
##### Section 4.6. Exceptions
##### Section 4.7. Augmenting Types
##### Section 4.8. Recursion
##### Section 4.9. Scope
##### Section 4.10. Closure
##### Section 4.11. Callbacks
##### Section 4.12. Module
##### Section 4.13. Cascade
##### Section 4.14. Curry
##### Section 4.15. Memoization
##### Chapter 5. Inheritance
##### Section 5.1. Pseudoclassical
##### Section 5.2. Object Specifiers
##### Section 5.3. Prototypal11
##### Section 5.4. Functional
##### Section 5.5. Parts
##### Chapter 6. Arrays
##### Section 6.1. Array Literals
##### Section 6.2. Length
##### Section 6.3. Delete
##### Section 6.4. Enumeration
##### Section 6.5. Confusion
##### Section 6.6. Methods
##### Section 6.7. Dimensions
##### Chapter 7. Regular Expressions
##### Section 7.1. An Example
##### Section 7.2. Construction
##### Section 7.3. Elements
##### Chapter 8. Methods
##### Chapter 9. Style
##### Chapter 10. Beautiful Features
##### Appendix A. Awful Parts
##### Section A.1. Global Variables
##### Section A.2. Scope
##### Section A.3. Semicolon Insertion
##### Section A.4. Reserved Words
##### Section A.5. Unicode
##### Section A.6. typeof
##### Section A.7. parseInt
##### Section A.8. 
##### Section A.9. Floating Point
##### Section A.10. NaN
##### Section A.11. Phony Arrays
##### Section A.12. Falsy Values
##### Section A.13. hasOwnProperty
##### Section A.14. Object
##### Appendix B. Bad Parts
##### Section B.1. ==
##### Section B.2. with Statement
##### Section B.3. eval
##### Section B.4. continue Statement
##### Section B.5. switch Fall Through
##### Section B.6. Block-less Statements
##### Section B.7. ++ --
##### Section B.8. Bitwise Operators
##### Section B.9. The function Statement Versus the function Expression
##### Section B.10. Typed Wrappers
##### Section B.11. new
##### Section B.12. void
##### Appendix C. JSLint
##### Section C.1. Undefined Variables and Functions
##### Section C.2. Members
##### Section C.3. Options
##### Section C.4. Semicolon
##### Section C.5. Line Breaking
##### Section C.6. Comma
##### Section C.7. Required Blocks
##### Section C.8. Forbidden Blocks22
##### Section C.9. Expression Statements
##### Section C.10. for in Statement
##### Section C.11. switch Statement
##### Section C.12. var Statement
##### Section C.13. with Statement
##### Section C.14. =
##### Section C.15. == and !=
##### Section C.16. Labels
##### Section C.17. Unreachable Code
##### Section C.18. Confusing Pluses and Minuses
##### Section C.19. ++ and --
##### Section C.20. Bitwise Operators
##### Section C.21. eval Is Evil
##### Section C.22. void
##### Section C.23. Regular Expressions
##### Section C.24. Constructors and new
##### Section C.25. Not Looked For
##### Section C.26. HTML
##### Section C.27. JSON
##### Section C.28. Report
##### Appendix D. Syntax Diagrams
##### Appendix E. JSON
##### Section E.1. JSON Syntax
##### Section E.2. Using JSON Securely
##### Section E.3. A JSON Parser
##### Colophon
##### Index33

# Chapter 1: Good parts
## 1.1 - Why is JavaScript?
   - Js is the loose typing language when compair with other language
     - As in java, when you create a function with argument is string then call that funtion and pass a number, complier with detect errors for you, but with Js...nothing happens
   - Js is an important language because of it is language of web browser
     - If you wanna develop web, There is no choice but to JS
   - Js is built on some very good ideas and have few very bad ones
     - Good ideas: function, loose typing, dynamic object, an expressive object literal notation. (Object can be created by listing their components)
     - Bad ideas: is a programming language base on global variables, all of the top-level variables of all compilation units are tossed together in a common namespace called the global object (window), imagine when create file a.js have function a(), variable aVar and then create b.js, in b.js you can call a() and aVar.
> There are two answers:
>The first is that you don't have a choice. The Web hasbecome an important platform for application development, and JavaScript is the only language that is found in all browsers

> The other answer is that, despite its deficiencies, JavaScript is really good. It is lightweight and expressive. And once you get the hang of it, functional programming is a lot of fun
## 1.3 - A Simple Testing Ground
   - If you have a web browser and any text editor, you have everything you need to run JavaScript programs
> First, make an HTML file with a name like program.html:
```
<html>
    <body>
        <pre><script src="program.js"></script></pre>
    </body>
</html>
```
> Then, make a file in the same directory with a name like program.js:
```
document.writeln('Hello, world!');
```
> Open file program.html on browser

> Result: Hello, world!

# Chapter 2 - Grammar
## 2.1. White space
- Whitespace can take the form of formatting characters or comments
- Whitespace is usually insignificant, but itis occasionally necessary to use whitespace to separate sequences of characters that would otherwise becombined into a single token. For example, in:

```
var that = this;
```
> The space between var and that cannot be removed, but the other spaces can be removed.

- JavaScript offers two forms of comments, block comments formed with `/* */` and line-ending commentsstarting with `//`
- Comments should be used liberally to improve the readability of your programs
- Take carethat the comments always accurately describe the code
- Meaningless comments are worse than no comments
- In JavaScript, `/* */` can be occur in regular expression literals, so block comments are not safe for commenting out blocks of code. For example:
```
/*
  var rm_a = /a*/.match(s);
*/
```
> syntax error. So this form is not recommended, use `//` instead

## 2.2. Names
- A name is a letter optionally followed by one or more letters, digits, or under-bars. A name cannot be one of these reserved words:

`abstract boolean break byte case catch char class const continue debugger default delete do double else enum export extends false final finally float for function goto if implements import in instance of int interface long native new null package private protected public return short static super switch synchronized this throw throws transient true try type of var volatile void while with`

- It is not permitted to name a variable or parameter with a reserved word
- Names are used for statements, variables, parameters, property names, operators, and labels.
## 2.3. Numbers
- JavaScript has a single number type. Internally, it is represented as 64-bit floating point, same Java's double 
- Unlike most other programming languages, there is no separate integer type
> so 1 and 1.0 are the same value

> All you need to know about a number is that it is a number
- If a number literal has an exponent part, then the value of the literal is computed by multiplying the part before the e by 10 raised to the power of the part after the e
> So 100 and 1e2 are the same number.
- Negative numbers can be formed by using the - prefix operator.
> -1, -2, ......
- The value NaN is a number value that is the result of an operation that cannot produce a normal result. NaN is not equal to any value, including itself
> 10 - "a" => NaN

> You can detect NaN with the isNaN(number) function.
- The value Infinity represents all values greater than 1.79769313486231570e+308.
- JavaScript has a Math object that contains a set of methods that acton numbers. For example:
```
Math.floor(number)
```

## 2.4. Strings
- A string literal can be wrapped in single quotes or double quotes.
- The\ (backslash) is the escape character
- JavaScript was built at a time when Unicode was a 16-bit character set,so all characters in JavaScript are - The escape sequences allow for inserting characters into strings that are not normally permitted, such as backslashes, quotes, and control characters
> const text = "test escape \\\\, \'"
> - result:  test escape \\, '
- The \u convention allows for specifying character code points.
> "A" === "\u0041"
- Strings have a length property. For example, `"seven".length is 5`
- Strings are immutable. Once it is made, a string can never be changed. But it is easy to make a new string by concatenating other strings together with the + operator
- Two strings containing exactly the same characters in the same order are considered to be the same string. So:
`'c' + 'a' + 't' === 'cat'`
## 2.5. Statements
- When used inside of a function, the var and let statement defines the function's private variables.
- The switch, while, for, and do statements are allowed to have an optional label prefix that interacts with the break statement
- Statements tend to be executed in order from top to bottom. The sequence of execution can be altered by theconditional statements (if and switch), by the looping statements (while, for, and do), by the disruptivestatements (break, return, and throw), and by function invocation
- A block is a set of statements wrapped in curly braces. Unlike many other languages, blocks in JavaScript donot create a new scope, so variables should be defined at the top of the function, not in blocks. **(backward)**
- In JavaScript, statements like: if, while, ... will execute codes by the value of the expression, if value is truly, the code will be executed
- Have two expression's values: `truthy` and `falsy`
- Here are the falsy values:
```
false
null
undefined
The empty string ''
The number 0
The number NaN
```
> All other values are truthy, including true, the string 'false', and all objects

## 2.6. Expressions
- The simplest expressions are a literal value (such as a string or number), a variable, a built-in value (true,false, null, undefined, NaN, or Infinity)
- The ? ternary operator takes three operands. If the first operand is truthy, it produces the value of the second operand. But if the first operand is falsy, it produces the value of the third operand
```
1+1 > 0 ? console.log('true') : console.log('false');
```
> Result: true
- Parentheses can be used to alter the normal precedence, so:
```
2 + 3 * 5 === 17
(2 + 3) * 5 === 25
```
- The `+` operator adds or concatenates. If you want it to add, make sure both operands are numbers.
```
5 + 5 = 10;
"hel" + "lo" = "hello";
```
- The `/` operator can produce a non-integer result even if both operands are integers.
```
3 / 2 = 1.5;
```
- The `&&` operator produces the value of its first operand if the first operand is falsy. Otherwise, it produces the value of the second operand
```
const value = (2 < 1) && (2 > 1);
```
> value = false;
```
const value = (2 > 1) && "OK";
```
> value = "OK";
```
const value = (2 < 1) && "NOT OK";
```
> value = false;
```
true && console.log('Hi !');
```
> console: Hi !
- The || operator produces the value of its first operand if the first operand is truthy. Otherwise, it produces the value of the second operand
```
const value = (2 > 1) || (3 > 2);
```
> value = true;
```
const value = (2 < 1) || (2 > 1);
```
> value = true;
```
const value = (2 > 1) || "OK";
```
> value = true;
```
const value = (2 < 1) || "NOT OK";
```
> value = "NOT OK";
## 2.7. Literals
- Literals is a value that represent itself
> 12 , "Hello", ... is Literals
```
- number literal
- string literal
- Object literal
- arrays literal
- function
- regexp literal
```
- Object literals: 
  - Object literals are a convenient notation for specifying new objects.
  - The names of the properties can be specified as names or as strings.
  - The names are treated as literal names, not as variable names, so the names ofthe properties of the object must be known at compile time
  - The values of the properties are expressions.
- Array literals:
  - Array literals are a convenient notation for specifying new arrays

> There will be more about thats in the next characters
# Chapter 3
- The simple types of JavaScript are numbers, strings, booleans (true and false), null, and undefined.All other values are objects
- Numbers, strings, and booleans are object-like in that they have methods, butthey are immutable
- Objects in JavaScript are mutable keyed collections
- In JavaScript, arrays are objects,functions are objects, regular expressions are objects, and, of course, objects are objects
- An object is a container of properties, where a property has a name and a value. A property name can be any string, including the empty string
- Objects in JavaScript are class-free. There is no constraint on the names of new properties or on the values of properties
- JavaScript includes a prototype linkage feature that allows one object to inherit the properties of another.When used well, this can reduce object initialization time and memory consumption.
## 3.1. Object Literals
- An object literal is a pair of curly braces surrounding zero or more name/value pairs
```
var empty_object = {};

var stooge = {
  "first-name": "Jerome",
  "last-name": "Howard"
};
```
- A property's value can be obtained from any expression, including another object literal. Objects can nest:
```
var flight = {
    airline: "Oceanic",
    number: 815,
    departure: {
      IATA: "SYD",
      time: "2004-09-22 14:55",
      city: "Sydney"    
    },
    arrival: {
      IATA: "LAX",
      time: "2004-09-23 10:42",
      city: "Los Angeles"
    }    
};
```
## 3.2. Retrieval
- Values can be retrieved from an object by wrapping a string expression in a [ ] suffix. If the string expression is a constant, and if it is a legal JavaScript name and not a reserved word, then the . notation can be used instead
```
stooge["first-name"]     // "Joe"
flight.departure.IATA    // "SYD"
```
> The . notation is preferred because it is more compact and it reads better:
- The undefined value is produced if an attempt is made to retrieve a nonexistent member:
```
stooge["FIRST-NAME"]     // undefined
```
- The || operator can be used to fill in default values:
```
var middle = stooge["middle-name"] || "(none)";
var status = flight.status || "unknown";
```
- Attempting to retrieve values from undefined will throw a TypeError exception. This can be guarded against with the && operator:
```
flight.equipment                              // undefined
flight.equipment.model                        // throw "TypeError"
flight.equipment && flight.equipment.model    // undefined
```
## 3.3. Update
- A value in an object can be updated by assignment. If the property name already exists in the object, the property value is replaced:
```
stooge['first-name'] = 'Jerome';
```
- If the object does not already have that property name, the object is augmented
```
stooge['middle-name'] = 'Lester';
stooge.nickname = 'Curly';
flight.equipment = {    model: 'Boeing 777'};
flight.status = 'overdue';
```
## 3.4 Reference
- Objects are passed around by reference. They are never copied:
```
var x = stooge;x.nickname = 'Curly';
var nick = stooge.nickname;    // nick is 'Curly' because x and stooge are references to the same object
```

> Note:

> var a = {}, b = {}, c = {};
>> a, b, and c each refer to a different empty object

> a = b = c = {};
>> a, b, and c all refer to the same empty object
## 3.5. Prototype
- Every object is linked to a prototype object from which it can inherit properties. All objects created from object literals are linked to Object.prototype, an object that comes standard with JavaScript
- When you make a new object, you can select the object that should be its prototype. The mechanism thatJavaScript provides to do this is messy and complex, but it can be significantly simplified
```
var originalObj = { name: 'originalObj' };

if (type of Object.beget !== 'function') {
  Object.beget = function(object) {
    var F = function () { };
    F.property = object;
    return new F();
  }
}

var coppedObj = Object.beget(originalObj);

coppedObj.__proto__ = { name: 'originalObj' };

originalObj.color = 'red';

coppedObj.__proto__ = {
  name: 'originalObj',
  color: 'red'
};

coppedObj.name => 'originalObj';
coppedObj.color => 'red';

```
## 3.6. Reflection
- It is easy to inspect an object to determine what properties it has by attempting to retrieve the properties and examining the values obtained
- The typeof operator can be very helpful in determining the type of a property:
```
var flight = {
  number: 1,
  status: 'working',
  arrival: {
    country: 'VIETNAM'
  }
};

typeof flight.number      // 'number'
typeof flight.status      // 'string'
typeof flight.arrival     // 'object'
typeof flight.manifest    // 'undefined'
```
- Some care must be taken because any property on the prototype chain can produce a value:
```
typeof flight.toString    // 'function'
typeof flight.constructor // 'function'
```
- The hasOwnProperty method, which returns true if the object has aparticular property. The hasOwnProperty method does not look at the prototype chain: 
```
flight.hasOwnProperty('number')         // true
flight.hasOwnProperty('constructor')    // false
```
## 3.7. Enumeration
- The for in statement can loop over all of the property names in an object
- The enumeration will include all of the properties,including functions and prototype properties
```
var name;
for (name in another_stooge) {
      if (typeof another_stooge[name] !== 'function') {
        document.writeln(name + ': ' + another_stooge[name]);    
      }
}
```
- There is no guarantee on the order of the names, so be prepared for the names to appear in any order. If you want to assure that the properties appear in a particular order, we can make an array containing the names of the properties in the correct order:
```
var i;
var properties = [
  'first-name',
  'middle-name',
  'last-name',
  'profession'
];
for (i = 0; i < properties.length; i += 1) {
  document.writeln(properties[i] + ': ' + another_stooge[properties[i]]);
}
```
## 3.8. Delete
- The delete operator can be used to remove a property from an object. It will remove a property from the object if it has one. It will not touch any of the objects in the prototype linkage:
```
another_stooge.nickname    // 'Moe'

delete another_stooge.nickname;

another_stooge.nickname    // undefined
```
## 3.9. Global Abatement
- JavaScript makes it easy to define global variables that can hold all of the assets of your application, but global variables weaken the resiliency of programs and should be avoided.
- One way to minimize the use of global variables is to create a single global variable for application:
```
var MYAPP = {};
```
- That variable then becomes the container for your application:
```
MYAPP.stooge = {
  "first-name": "Joe",
  "last-name": "Howard"
}

MYAPP.flight = {
  airline: "Oceanic",
  number: 815,
  departure: {
    IATA: "SYD",
    time: "2004-09-22 14:55",
    city: "Sydney"
    },
    arrival: {
      IATA: "LAX",
      time: "2004-09-23 10:42",
      city: "Los Angeles"
      }
};
```
> By reducing your global footprint to a single name, you significantly reduce the chance of bad interactions with other applications, widgets, or libraries, Your program also becomes easier to read
