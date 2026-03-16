What is JavaScript?
•	JavaScript is a lightweight and interpreted programming language with object-oriented capacity but it is not fully object oriented capacity. 
•	It helps you to develop interactivity into static HTML pages.

Javascript is client side or server side?
Both.
•	Historically client-side: Runs in the browser to handle UI, DOM manipulation, events, and user interactions.
•	Now also server-side: Thanks to Node.js, JavaScript runs on the server to handle APIs, business logic, database access, and background jobs.

JavaScript 1Hoisting? (Temporal dead zone)
•	Hoisting is JavaScript's default behaviour of moving declarations to the top.
•	In JavaScript, a variable can be used before it has been declared.
•	Let and const are hoisted, but they are not initialized, In other words, you can't access their value before the declaration
Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top before code execution.
Remember that JavaScript only hoists declarations, not initialization. Let's take a simple example of variable hoisting,
console.log(message); //output : undefined
var message = 'The variable Has been hoisted';
The above code looks like as below to the interpreter,
var message;
console.log(message);
message = 'The variable Has been hoisted';


What is 1this?
The JavaScript this keyword refers to the current object of a class
It has different values depending on where it is used:
•	In a method, this refers to the owner object.
•	In a function, this refers to the global object.
•	In a function, in strict mode, this is undefined.
•	In an event, this refers to the element that received the event.
•	Methods like call(), and apply() can refer this to any object.
In strict mode, when used alone, this also refers to the Global object.

THIS keyword is used as a pointer which differentiates between the current object with the global object.

What data types do JavaScript support?
•	Number
•	String
•	Boolean
•	Undefined
•	Null
•	Symbol
•	Object


What is 1isNaN?
•	The isNaN() function is used to determine whether a value number of Not (Not-a-Number) 
•	This function returns true if the value equates to NaN. Otherwise it returns false.

isNaN('Hello') //true
isNaN('100') //false

1Overriding In Javascript?
•	JavaScript supports overriding not overloading. 
•	Meaning, that if you define two functions with the same name, the last one defined will override the previously defined version and every time a call will be made to the function, the last defined one will get executed.
•	Also Method overriding allows a child class to provide a specific implementation of a method that is already defined in its parent class, enabling more specialized behavior.

What is the 1super keyword used for in TypeScript?
The super keyword is used to call the constructor, properties, and methods of the parent class from the child class.


Does TypeScript support multiple inheritance?
No, TypeScript supports only single inheritance (one class can extend only one parent class) and multilevel inheritance (a class can extend a class that extends another class).

What is a 1Class in JavaScript?
A class in JavaScript is a blueprint for creating objects.
It encapsulates data (properties) and behavior (methods) into a single structure.
It provides a cleaner, more readable way to create objects and implement object oriented programming, but under the hood, it still uses prototypes.
extends is used for inheritance. 
super() is required in child constructor to access the parent constructor.
JavaScript classes do not introduce a new object model; they are still prototype-based.
What is Prototype?
Prototype is a mechanism in JavaScript through which objects inherit properties and methods from each other.
Everything in JS is prototype based.

What is constructor?
A constructor is a special method inside a class (or constructor function) that is executed when a new object is created. It initializes object properties.
•	Only one constructor is allowed per class. 
•	Automatically called when using new. 
•	Used to initialize state.

What is 1encapsulation?
Encapsulation restricts direct access to object data and exposes only necessary behavior
Encapsulation improves security and reduces unintended modifications.


JavaScript Class 1Inheritance
Inheritance allows one class to use the properties and methods of another class using extends and super().
•	To create a class inheritance, use the extends keyword.
•	A class created with a class inheritance inherits all the methods from another class
•	super() calls the parent constructor. 
•	Inheritance is useful for code reusability.

Difference between 1interface and class in javascript

A class is a blueprint from which we can create objects that share the same configuration - properties and methods. 
An interface is a group of related properties and methods that describe an object, but neither provides implementation nor initialisation for them.
 Interfaces contain only the declaration of the members.

A class describes the attributes and behaviors of an object. 
An interface contains behaviors that a class implements. 
A class may contain abstract methods, concrete methods. 
An interface contains only abstract methods.

Is JavaScript case-sensitive?
Yes, JavaScript is case-sensitive.

How can one create an object using JavaScript?
Since JavaScript is an Object-oriented programming scripting language, it supports the concept of Object. By using Object literal, you can create an object. 
var x = 10, y = 20
obj = { x, y }
console.log(obj); // {x: 10, y:20}

var object = 
        { 
         name: "obj",
         age: 10
         };

How can we read the properties of an object in js?
Can write and read properties of an object using the dot(.) notation.

How can one use JavaScript to create an Array?
If you want to define arrays in JavaScript, you can do so by using array literal. Example:
var x = [];
var y = [1, 2, 3, 4, 5];

An array has a length property that is useful for iteration. We can read elements of an array as follows
for (var i = 0; i < x.length; i++)

What is a 1callback function?
•	A callback function is a function passed into another function as an argument.
•	The Callback is a function that needs to be executed after another function has finished executing.
Let's take a simple example of how to use callback function
function callbackFunction(name) {
  console.log('Hello ' + name);
}
function outerFunction(callback) {
  let name = prompt('Please enter your name.');
  callback(name);
}

outerFunction(callbackFunction);



What are 1closures?
•	It is an inner function that has access to the outer function’s variables. 
•	Closure is developed when a specific variable is defined outside the current scope and it is accessed from within with some inner scope.  
The closure has three scope chains
1.Own scope where variables defined between its curly brackets
2.Outer function’s variables
3.Global variables 
Let's take an example of closure concept,

function Welcome(name){
  var greetingInfo = function(message){
   console.log(message+' '+name);
  }
return greetingInfo;
}
var myFunction = Welcome('John');
myFunction('Welcome '); //Output: Welcome John
myFunction('Hello Mr.'); //output: Hello Mr.John
As per the above code, the inner function(greeting Info) has access to the variables in the outer function scope(Welcome) even after outer function has returned.
Closure Function example:
You can create a closure to keep the value of a even after the inner function is returned. The inner function that is being returned is created within an outer function, making it a closure, and it has access to the variables within the outer function, in this case the variable a.

What is 1currying?
Currying is a JavaScript functional programming technique where a function that takes multiple arguments is transformed into a sequence of functions, each taking one argument at a time.
const multiply = a => b => a * b;
console.log(multiply(5)(6)); // 30


What are some of the 1built-in methods in JavaScript and what are the values returned by them?
Some of the built-in methods and the values returned by them are:
Concat() helps to join two or more than two strings
CharAt() helps to return the character at the specific index
forEach() helps to call a function for each element present in the array
length() helps to return the length of the string
indexOf() helps in returning the index within the calling String object of the first occurrence of the specific value
push() helps to add one or more than one element to the end of an array and then return the new length of that array
pop() helps to remove the last element from an array and return that element
reverse() helps to reverse the order of elements of an array
includes() The includes() method returns true if a string contains a specified string Otherwise it returns false. 
string.includes(searchvalue, start) 
searchvalue - Required. The string to search for
start - Optional. The position to start from. Default value is 0

What is typeof operator?
You can use the JavaScript typeof operator to find the type of a JavaScript variable. It returns the type of a variable or an expression.
The specified operand can be a data structure or a literal such as a function, object or a variable.
typeof "John Abraham"     // Returns "string"
typeof (1 + 2)        // Returns "number"

What are various operators supported by javascript
i.	Arithmetic Operators: Includes + (Addition),– (Subtraction), * (Multiplication), / (Division), % (Modulus), + + (Increment) and – – (Decrement)
ii.	Comparison Operators: Includes = =(Equal),!= (Not Equal), ===(Equal with type), > (Greater than),> = (Greater than or Equal to),< (Less than),<= (Less than or Equal to)
iii.	Logical Operators: Includes &&(Logical AND),||(Logical OR),!(Logical NOT)
iv.	Assignment Operators: Includes = (Assignment Operator), += (Add and Assignment Operator), – = (Subtract and Assignment Operator), *= (Multiply and Assignment), /= (Divide and Assignment), %= (Modules and Assignment)
v.	Ternary Operators: It includes conditional(: ?) Operator
vi.	typeof Operator: It uses to find type of variable. The syntax looks like typeof variable

What is a 1Cookie?
•	A cookie is a piece of data that is stored on your computer to be accessed by your browser. 
•	Cookies are saved as key-value pairs. For example, you can create a cookie named username as below
document.cookie = "username=John";

How are 1Attributes different from Property?
Attribute provides more details of an element like type, id, value, etc.
Property is the specific value assigned to the property. For example, value = ‘Name’, type = “text”, etc.

Give a list of the various ways using which an HTML element can be accessed within a JavaScript code?
A few ways are:
•getElementById(‘idname’): Using this method, you can get an element by the ID name of the element.
•getElementsByClass(‘classname’): Using this method, you can get all elements which have a given classname.
•getElementsByTagName(‘tagname’): Using this method, you can get all elements which have a given tag name.
•querySelector(): The querySelector() function takes the css style selector and returns the first selected element.


How are the JavaScript 1window and JavaScript 1document different from one another?
Window is a global object, and it holds functions, variables, location and history.
Document is a part of the window and is considered one of its properties in JavaScript.

How are 1innerText and 1innerHTML different?
innerText – innerText does not process an HTML tag if it is found within a string.
innerHTML – innerHTML processes an HTML tag if it is found within a string.
https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_node_innertext

What are break and continue statements?
The break statement is used to jumps out of a loop. i.e, It breaks the loop and continues executing the code after the loop.
for (i = 0; i < 10; i++) {
  if (i === 5) { break; }
  text += "Number: " + i + "<br>";
}
The continue statement is used to jumps over one iteration in the loop. i.e, It breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.
for (i = 0; i < 10; i++) {
    if (i === 5) { continue; }
    text += "Number: " + i + "<br>";
}

What is event 1bubbling?
Event bubbling is a type of event propagation where the event first triggers on the innermost target element, and then successively triggers on the parents (ancestors) of the target element in the same nesting hierarchy till it reaches the outermost DOM element. (child to parent)
What is event 1capturing?
Event capturing is a type of event propagation where the event is first captured by the outermost element, and then successively triggers on the children (descendants) of the target element in the same nesting hierarchy till it reaches the innermost DOM element. (parent to child)
What are the differences between undeclared and 1undefined variables?
Below are the major differences between undeclared and undefined variables,

What is the difference between null and 1undefined?

What is known as the Strict mode and how can you enable it?
•	The Strict mode helps you to check errors in your code. 
•	Strict mode is useful to write "secure" JavaScript by notifying "bad syntax" into real errors.
•	In this mode the code throws all types of error.
•	When you are using strict mode, you will not be able to use implicitly declared variables nor can you assign any value to read-only property.  
•	If you want to enable the strict mode, all you have to do is add “use strict” at the start of a program, function or file.

The main differences between 1filter and find?
1.	filter() returns an array containing the element that satisfies the condition, but find() returns the element itself that satisfies the condition.
2.	In filter(), whole array is iterated despite the fact that the element being searched for is present at the beginning. But in find(), as soon as the element that satisfies the condition is found, it gets returned.

In JavaScript, what is the use of the prompt box?
JavaScript has three kind of popup boxes: Alert box, Confirm box, and Prompt box.
Alert Box:
An alert box is often used if you want to make sure information comes through to the user.
When an alert box pops up, the user will have to click "OK" to proceed.

Confirm Box:
A confirm box is often used if you want the user to verify or accept something.
When a confirm box pops up, the user will have to click either "OK" or "Cancel" to proceed.
If the user clicks "OK", the box returns true. If the user clicks "Cancel", the box returns false.

Prompt Box:
A prompt box is often used if you want the user to input.
When a prompt box pops up, the user will have to click either "OK" or "Cancel" to proceed after entering an input value.
If the user clicks "OK" the box returns the input value. If the user clicks "Cancel" the box returns null.

What is the difference between 1Call, 1Apply and 1Bind methos?

Call: runs a function using a specific ‘this’ value and passes arguments one by one.
fun.call(thisArg[, arg1[, arg2[, …]]])
function greet() {
  console.log("Hello, " + this.name);
}
const person = { name: "Pravin" };
greet.call(person); // Output: Hello, Pravi

Apply: Runs the function and lets you pass arguments as an array.
fun.apply(thisArg, [argsArray])
function addNumbers(a, b, c) {
  console.log(a + b + c);
}
const numbers = [2, 3, 5];
addNumbers.apply(null, numbers); // Output: 1

bind: It creates a new function that accepts array and any number of arguments.
const person = {
  name: "Pravin",
  greet() {
    console.log("Hello, " + this.name);
  }
};
const newGreet = person.greet.bind(person);
newGreet(); // Output: Hello, Pravin

•	Call and apply are interchangeable. Both execute the current function immediately. 
•	You need to decide whether it’s easier to send in an array or a comma separated list of arguments. 
•	You can remember by treating Call is for comma (separated list) and Apply is for Array. 
What is 1JSON and its common operations?
•	JSON is a text-based data format following JavaScript object Notation/syntax.
•	It is useful when you want to transmit data across a network and it is basically just a text file with an extension of .json, and a MIME type of application/json 

Parsing: Converting a string to a native object
JSON.parse(text)
Stringification: **converting a native object to a string so it can be transmitted across the network
JSON.stringify(object)


What is the purpose of array 1slice method?
The slice() method returns the selected elements in an array as a new array object. 
It selects the elements starting at the given start argument and ends at the given optional end argument without including the last element. 
If you omit the second argument then it selects till the end. Some of the examples of this method are,
let arrayIntegers = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegers.slice(0,2); // returns [1,2]
let arrayIntegers2 = arrayIntegers.slice(2,3); // returns [3]
let arrayIntegers3 = arrayIntegers.slice(4); //returns [5]
Note: Slice method won't mutate the original array but it returns the subset as new array.

What is the purpose of array 1splice method?
The splice() method is used either adds/removes items from an array, and then returns the removed item. 
The first argument specifies the array position for insertion or deletion whereas the option second argument indicates the number of elements to be deleted. 
Each additional argument is added to the array. Some of the examples of this method are,
let arrayIntegersOriginal1 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal2 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal3 = [1, 2, 3, 4, 5];

let arrayIntegers1 = arrayIntegersOriginal1.splice(0,2); // returns [1, 2]; original array: [3, 4, 5]
let arrayIntegers2 = arrayIntegersOriginal2.splice(3); // returns [4, 5]; original array: [1, 2, 3]
let arrayIntegers3 = arrayIntegersOriginal3.splice(3, 1, "a", "b", "c"); //returns [4]; original array: [1, 2, 3, "a", "b", "c", 5]
Note: Splice method modifies the original array and returns the deleted array.


What is 1scope in javascript?
Scope is the accessibility of variables, functions, and objects in some particular part of your code during runtime.
1.	Global 
2.	Local.

Global scope refers to variables or functions that are declared outside of any function or block.
These can be accessed from anywhere in the program.

Local scope refers to variables declared inside a function or block.
These variables can be accessed only within that function/block.
What is IndexedDB?
IndexedDB is a low-level API for client-side storage of larger amounts of structured data, including files/blobs. 
This API uses indexes to enable high-performance searches of this data.

What is the difference between == and 1=== operators?	
•	= is used for assigning values to a variable, 
== is used for comparing two variables, but it ignores the datatype of variable 
=== is used for comparing two variables, but this operator also checks datatype and compares two values.
•	= is called as assignment operator, 
== is called as comparison operator.
=== is called as strict operator.
•	= does not return true or false, 
== Return true only if the two operands are equal, while 
=== returns true only if both values and data types are the same for the two variables. 
The strict operators follow the below conditions for different types,
i.	Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions.
ii.	Two numbers are strictly equal when they are numerically equal. i.e, Having the same number value. There are two special cases in this,
a.	NaN is not equal to anything, including NaN.
b.	Positive and negative zeros are equal to one another.
iii.	Two Boolean operands are strictly equal if both are true or both are false.
iv.	Two objects are strictly equal if they refer to the same Object.
v.	Null and Undefined types are not equal with ===, but equal with ==. 
a.	i.e, null===undefined --> false but null==undefined --> true

0 == false   // true
0 === false  // false
1 == "1"     // true
1 === "1"    // false
null == undefined // true
null === undefined // false
'0' == false // true
'0' === false // false
[]==[] or []===[] //false, refer different objects in memory
{}=={} or {}==={} //false, refer different objects in memory


/* Here, '5' will be converted to 5 */	
	5 == '5'; // true
	5 === '5'; // false
	
	/* Here, true will be converted to 1 */
	1 == true; // true
	1 > false; // true
	0 === false; // false
	
	// Here, JS will try to convert both of these to number
	// Number('true') = NaN (Not a Number), but Number(true) = 1
	'true' == true; // false
	'true' === true; // false


In JavaScript, objects are a 1reference type.
It compares object references, not their content. 
Array in JavaScript are objects, and each array instance has a unique reference in memory. Even if two arrays contain the same elements, they are considered different objects and thus have different references.
To compare the concept of array, you would need to check each element individually, or use methods like array.prototype.every() or libraries that provide deep comparison functions

Example:
function arrayEqual(arr1, arr2) {
  return (arr1.length == arr2.length) &&
  (arr1.every((value, index) => 
    value === arr2[index]  
  ))
}
console.log(arrayEqual([1,2,3], [1,2,3]));

What is an 1anonymous function?
An anonymous function is a function without a name. 
Anonymous functions are commonly assigned to a variable name or used as a callback function. 
The syntax would be as below,
function (optionalParameters) {
  //do something
}
const myFunction = function(){ //Anonymous function assigned to a variable
  //do something
};
[1, 2, 3].map(function(element){ //Anonymous function used as a callback function
  //do something
});
Let's see the above anonymous function in an example,
var x = function (a, b) {return a * b};
var z = x(5, 10);
console.log(z); // 50


What are 1lambda or 1arrow functions?
An arrow function is a shorter syntax for a function expression and does not have its own this, arguments, super, or new.target. 
These functions are best suited for non-method functions, and they cannot be used as constructors.
Before:
hello = function() {
  return "Hello World!";
}

After:
hello = () => {
  return "Hello World!";
}
Note: This works only if the function has only one statement.

What is a 1Regular Expression
A regular expression is a sequence of characters that forms a search pattern. 
You can use this search pattern for searching data in a text. These can be used to perform all types of text search and text replace operations.

The Difference Between 1var, 1let and 1const in JavaScript

• var declarations are globally/Functional scoped while let and const are block scoped.
• var variables can be updated and re-declared within its scope; let variables can be updated but not re-declared; const variables can neither be updated nor re-declared.
• They are all hoisted to the top of their scope. But while var variables are initialized with undefined, let and const variables are not initialized.
• While var and let can be declared without being initialized, const must be initialized during declaration.
• Var is been available from the beginning of JavaScript and let and const Introduced as part of ES6.
 

 
	function doStuff() {
	// both a and b will be available for this function, but not outside
	let a = 5;
	var b = 5;
	console.log(a + b); // 10
	}
	
	doStuff(); // 10;
	console.log(a); // ReferenceError
	console.log(b); // ReferenceError
	
	function doMoreStuff() {
	if (2 + 2 === 4) {
	// Here, a will be available for the whole function
	var a = 5;
	// But b will be available only inside this if block
	let b = 5;
	}
	console.log(a); // 5
	console.log(b); // ReferenceError
	}
	
	doMoreStuff();
	// 5
	// ReferenceError
	
	for (let i = 0; i < 5; i++) {
	// i is re-created on every interation
	// and setTimeout gets a new i every time
	setTimeout(() => console.log(i), 100);
	}
	/*
	0
	1
	2
	3
	4
	*/
	
	for (var j = 0; j < 5; j++) {
	// j is scoped to the outside function (which is the file itself)
	// thus, it is not recreated and setTimeout gets the same reference to j
	setTimeout(() => console.log(j), 100);
	}
	/*
	5
	5
	5
	5
	5
	*/
 


https://alligator.io/js/var-let-const/

1Spread vs 1Rest operator in JavaScript ES6
Both represented by three dots (…)
Both rest parameter and spread operator were introduced in the ES6 version of javascript.

1Rest Parameter/Operator:
•	In functions when we require to pass arguments but were not sure how many we have to pass that time we use rest parameter
•	Any number of arguments will be converted into an array using the rest parameter.
•	Rest parameters can be used by applying three dots (...) before the parameters.
function extractingArgs(...args){
  return args[1];
}

// extractingArgs(8,9,1); // Returns 9

function addAllArgs(...args){
  let sumOfArgs = 0;
  let i = 0;
  while(i < args.length){
    sumOfArgs += args[i];
    i++;
  }
  return sumOfArgs;
}

addAllArgs(6, 5, 7, 99); // Returns 117
addAllArgs(1, 3, 4); // Returns 8

function abc(a, ...rest) {
return rest;
}
console.log(abc(10, 1, 2, 3, 4, 5));
**Note- Rest parameter should always be used at the last parameter of a function.
// Incorrect way to use rest parameter
function randomFunc(a,...args,c){
//Do something
}

// Correct way to use rest parameter
function randomFunc2(a,b,...args){
//Do something
}
1Spread operator (…) 
•	The spread operator (...) expands arrays or objects into individual elements/properties.
•	It’s like taking a bunch of items from a box and laying them out separately on a table.
•	I use it to create shallow copies, merge arrays/objects, and pass array values as function args.
•	In TypeScript, the spread operator (in form of ellipsis) can be used to initialize arrays/objects from another array/object.
•	The spread operator is a useful and quick syntax for adding items, combining, and spreading out an array/object into a function’s arguments.
•	It supports immutable (not changing original data) patterns nicely, but it’s a shallow copy so nested structures are still shared. Means - When you use the spread operator (...), you usually create a new copy instead of changing the original. It only copies the top level. If your object/array has nested objects/arrays inside, those inner parts are still linked to the original

function addFourNumbers(num1,num2,num3,num4){
  return num1 + num2 + num3 + num4;
}

let fourNumbers = [5, 6, 7, 8];


addFourNumbers(...fourNumbers);
// Spreads [5,6,7,8] as 5,6,7,8

let array1 = [3, 4, 5, 6];
let clonedArray1 = [...array1];
// Spreads the array into 3,4,5,6
console.log(clonedArray1); // Outputs [3,4,5,6]


let obj1 = {x:'Hello', y:'Bye'};
let clonedObj1 = {...obj1}; // Spreads and clones obj1
console.log(obj1);

let obj2 = {z:'Yes', a:'No'};
let mergedObj = {...obj1, ...obj2}; // Spreads both the objects and merges it
console.log(mergedObj);
// Outputs {x:'Hello', y:'Bye',z:'Yes',a:'No'};
***Note- Key differences between rest parameter and spread operator:
•	Rest parameter is used to take a variable number of arguments and turns them into an array while the spread operator takes an array or an object and spreads it
•	Rest parameter is used in function declaration whereas the spread operator is used in function calls
•	The main difference between the two operators lies in their names. The spread operator in JavaScript expands values in arrays and strings into individual elements whereas, the rest operator, puts the values of user-specified data into a JavaScript array.
•	Rest Operator should be used as last parameter
•	Spread operator can be use at any position
•	There must be only one rest parameter in javascript functions.
•	There can be more than one spread operator in javascript functions.

How do you 1trim a string in javascript?
JavaScript provided a trim method on string types to trim any whitespaces present at the begining or ending of the string.
"  Hello World   ".trim(); //Hello World
If your browser(<IE9) doesn't support this method then you can use below polyfill.
if (!String.prototype.trim) {
    (function() {
        // Make sure we trim BOM and NBSP
        var rtrim = /^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g;
        String.prototype.trim = function() {
            return this.replace(rtrim, '');
        };
    })();
}

How do you trim a string at the beginning or ending?
The trim method of string prototype is used to trim on both sides of a string. 
But if you want to trim especially at the beginning or ending of the string then you can use trimStart/trimLeft and trimEnd/trimRight methods. 
Let's see an example of these methods on a greeting message,
var greeting = '   Hello, Goodmorning!   ';

console.log(greeting); // "   Hello, Goodmorning!   "
console.log(greeting.trimStart()); // "Hello, Goodmorning!   "
console.log(greeting.trimLeft()); // "Hello, Goodmorning!   "

console.log(greeting.trimEnd()); // "   Hello, Goodmorning!"
console.log(greeting.trimRight()); // "   Hello, Goodmorning!"

What is AJAX?
AJAX stands for Asynchronous JavaScript and XML and it is a group of related technologies(HTML, CSS, JavaScript, XMLHttpRequest API etc) used to display data asynchronously. i.e. We can send data to the server and get data from the server without reloading the web page.

What is Synchronous?

JavaScript is single threaded, meaning it executes one statement at a time, in top to bottom order.
This is called synchronous or blocking execution.

In synchronous execution, each line waits for the previous one to finish. If one task takes time, it blocks the entire thread.


What is Asynchronous?

Asynchronous JS allows tasks to run without blocking the main thread.
Long-running operations (API calls, timers, file reads) run in the background, while JS continues executing

Asynchronous JavaScript uses callbacks, promises, and async/await to handle non blocking operations.

JavaScript is synchronous by default, but async behavior is enabled by the event loop, which manages callback queues and promises.

What is an async function?
Async function is a function that always returns a Promise, even if you don't return one manually.
Async makes a function return a promise; await pauses execution inside that function until the promise resolves


These functions can contain zero or more await expressions.
Let's take a below async function example,
async function logger() {

  let data = await fetch('http://someapi.com/users'); // pause until fetch returns
  console.log(data)
}
logger();

What's a JavaScript 1Promise?
A Promise is a placeholder for a value that might not be available yet, but will be resolved in the future.
It allows you to write asynchronous code in a more manageable and readable way compared to traditional callbacks.
In short - 
A Promise represents a future value.
You use .then() to handle success and .catch() for errors.
Promises improve asynchronous code readability.

A Promise has 3 possible states:
Pending	Initial state, operation not finished yet
Fulfilled	Operation completed successfully, value is available
Rejected	Operation failed, reason (error) is available
Example -
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error("Error:", error);
  });

// Async example
async function fetchData() {
  try {
    let response = await fetch('https://api.example.com/data');
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}
fetchData();

Why use Promises?
•	To avoid callback hell (nested callbacks that are hard to read and maintain).
•	To handle asynchronous operations like fetching data from a server, reading files, timers, etc.
•	Centralize error handling with .catch()
•	They make chaining multiple async operations easier and cleaner.

What is the difference between 1Shallow and 1Deep copy
There are two ways to copy an object or arrays.
Shallow Copy: 
A shallow copy creates a new object or array, but only copies references to nested objects or arrays - not the actual inner values. So if you modify a nested element, it affects both the original and the copy.
If any of the fields of the object are references to other objects, just the reference addresses are copied i.e., only the memory address is copied.
Example
var empDetails = {
  name: "John", age: 25, expertise: "Software Developer"
}
to create a duplicate
var empDetailsShallowCopy = empDetails    // Shallow copying!
if we change some property value in the duplicate one like this:
empDetailsShallowCopy.name = "Johnson"

The above statement will also change the name of empDetails, since we have a shallow copy. That means we're losing the original data as well.

Example2: 
let original = {
  name: "Alice",
  address: {
    city: "New York"
  }
};
let shallowCopy = { ...original };
shallowCopy.address.city = "Los Angeles";
console.log(original.address.city);   // Output: "Los Angeles"
console.log(shallowCopy.address.city); // Output: "Los Angeles"
Deep copy: 
A deep copy creates a completely independent copy of the object and all nested structures.
Example
var empDetails = {
  name: "John", age: 25, expertise: "Software Developer"
}
Create a deep copy by using the properties from the original object into new variable
var empDetailsDeepCopy = {
  name: empDetails.name,
  age: empDetails.age,
  expertise: empDetails.expertise
}

Now if you change empDetailsDeepCopy.name, it will only affect empDetailsDeepCopy & not empDetails

Example2
let original = {
  name: "Alice",
  address: {
    city: "New York"
  }
};

// Deep copy using structuredClone (modern browsers)
let deepCopy = structuredClone(original);
deepCopy.address.city = "Los Angeles";
console.log(original.address.city);   // Output: "New York"
console.log(deepCopy.address.city);   // Output: "Los Angeles"


Arr2 = arr vs arr2 = ([…arr]) What is the difference?
let arr1 = [1, 2, 3]; 
// let arr2 = arr1;
let arr2 = [...arr1]
arr2.push(9);
console.log(arr1 === arr2);
// deep, shalow copy // output=> true // output=> false

It’s a shallow copy
You aren’t copying the array, but are copying the address of the array. So, you still have only one copy of the array, but two addresses that point to the same array. 
You are not sending the array itself but the address of it, also called “by reference”.

a = [1, 2, 3]; 
b = [1, 2, 3]; 
console.log(a == b); // false 
c = a; 
console.log(a === c); // true
---------------------------------------------
let nestedArray = [1, [2], 3];
let arrayCopy = JSON.parse(JSON.stringify(nestedArray)); // This is deep copy
let arrayCopy = [...nestedArray]; // This is shallow copy
---------------------------------------------------------
const numbers = [1, [2], [3, [4]], 5];
JSON.parse(JSON.stringify(numbers));  // Using JavaScript
_.cloneDeep(numbers);   // Using Lodash

Why does [1, 2] == [1, 2] return false in JavaScript?. (Answer: Arrays are compared by reference, not value, so two distinct arrays in memory are never equal by value comparison)


What is a Recursive Function?

Function calling itself inside its body again and again until it doesn’t have left with it anymore.

function factorial(n) {
  if (n === 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
console.log(factorial(5)); //120
-------------------------------------------------------------
let decrementCounter = (number) => {
 
        // Base case condition....
        if(number === 0) return; 
        console.log(number);
        decrementCounter(number - 1);
    }
    decrementCounter(5);



Coding Questions

What would be the result of 1+2+'3'?
The output is going to be 33. Since 1 and 2 are numeric values, the result of first two digits is going to be a numeric value 3. The next digit is a string type value because of that the addition of numeric value 3 and string type value 3 is just going to be a concatenation value 33.

NaN === NaN?
False. This is an endless source of debate and one of the most confusing parts about JS. In a nutshell, NaN stands for Not a Number, and just because one value is not a number and another one is not a number does not imply they are equal. The downside is you cannot really check if a variable is NaN using myVariable === NaN. You can use the Number.isNaN function or myVariable !== myVariable to check for it.
0.1 + 0.2 === 0.3?
False. This trick does not apply only to JS: it is common among floating-point operations in any language. It has to do with the way the CPU processes floating-point numbers. The actual value of 0.1 + 0.2 will be something like 0.300000001 and to check for equality you would write Math.abs(0.3 - (0.2 + 0.1)) <= EPS, where EPS is an arbitrary small value (0.00001, for example).

What is the output of below code?
console.log(1 < 2 < 3);
console.log(3 > 2 > 1);
Answer: true, false
The important point is that if the statement contains same operators(e.g, < or >) then it be evaluated from left to right. The first statement follows the below order,
1.console.log(1 < 2 < 3);
2.console.log(true < 3);
3.console.log(1 < 3); // True converted as 1 during comparision
4.True
Whereas the second statement follows the below order,
1.console.log(3 > 2 > 1);
2.console.log(true > 1);
3.console.log(1 > 1); // False converted as 0 during comparision
4.False
What is the output of below code?
const arrowFunc = () => arguments.length;
console.log(arrowFunc(1, 2, 3));
Answer: ReferenceError: arguments is not defined
Arrow functions do not have an arguments, super, this, or new.target bindings. So any reference to arguments variable tries to resolve to a binding in a lexically enclosing environment. In this case, the arguments variable is not defined outside of the arrow function. Hence, you will receive reference error.
Where as the normal function provides the number of arguments passed to the function
const func = function () {
                    return arguments.length;
                    }
console.log(func(1, 2, 3));

What is the output of below code?
console.log( String.prototype.trimLeft.name === 'trimLeft' );
console.log( String.prototype.trimLeft.name === 'trimStart' );
Answer: True, False
In order to be consistent with functions like String.prototype.padStart, the standard method name for trimming the whitespaces is considered as trimStart. Due to web compatibility reasons, the old method name 'trimLeft' still act as a alias for 'trimStart'. Hence, the prototype for 'trimLeft' is always 'trimStart'

What is the output of below code?
console.log(Math.max());
Answer: -Infinity
-Infinity is the initial comparant because almost every other value is bigger. So when no arguments are provided, -Infinity is going to returned. 
Note: Zero number of arguments is a valid case.

What is the output of below code?
console.log(10 === [10]);
console.log(10 === [[[[[[[10]]]]]]]);
Answer: True, True
As per the comparison algorithm in the ECMAScript specification(ECMA-262), the above expression converted into JS as below
10 === Number([10].valueOf().toString()) // 10
So it doesn't matter about number brackets([]) around the number, it always converted to a number in the expression.
What is the output of below code?
console.log(1 +  +"2" + "2"); // “32”
console.log(1 +  -"1" + "2"); // 02
console.log( "A" - "B" + "2"); // NaN2
console.log( "A" - "B" + 2) // NaN
console.log(“1” - -  “1”) // 2 => 1 – (-1) // 1+1
console.log(10 + '10');
console.log(10 - '10');
Answer: 1010, 0
The concatenation operator(+) is applicable for both number and string types. So if any operand is string type then both operands concatenated as strings. Whereas substract(-) operator tries to convert the operands as number type.

What is the output of below code?
const numbers = new Set([1, 1, 2, 3, 4]);
console.log(numbers);

const browser = new Set('Firefox);
console.log(browser);
Answer: {1, 2, 3, 4}, {"F", "i", "r", "e", "f", "o", "x"}
Since Set object is a collection of unique values, it won't allow duplicate values in the collection. At the same time, it is case sensitive data structure.

What is the output of below code?
console.log(NaN === NaN);
Answer: False
JavaScript follows IEEE 754 spec standards. As per this spec, NaNs are never equal for floating-point numbers.
console.log(typeof NaN === "number");  // logs "true"


Write a JavaScript function to check if a given string is a palindrome
function isPalindrome(str) { 
  return str === str.split(”).reverse().join(”); 
}
-----------------------------------------------------------------------------------
function isPalindrome(str) {
    const clnstr = str.replace(/[^a-zA-Z0-9]/g,'').toLowerCase();  // const re = /[\W_]/g;
    const charArr = clnstr.split('');
    const rvrstr = charArr.reverse();
    const resstr = rvrstr.join('');
    console.log(resstr);
    return clnstr === resstr;
}
const teststr = "Nitin";
console.log( isPalindrome(teststr) );

Write a JavaScript program to reverse a given string. 
const reverseString = (str) => str.split(”).reverse().join(”); 
------------------------------------------------
function resersWord(sentence) {
     const wordArr = sentence.split(" ");     
     const revWordArr = wordArr.reverse();
     const revSen = revWordArr.join(' ');
     return revSen;
 }
 const inSen = "Today is Monday";
 console.log(inSen);
 const res = resersWord(inSen);
 console.log(res);
----------------------------------------------------------------------

function resersWord(sentence) {
     const wordArr = sentence.split(" ");
     const revWordArr = [];
     for(let i = wordArr.length; i>=0;i--) {
         revWordArr.push(wordArr[i]);
     }
     const revSen = revWordArr.join(' ');
     return revSen;
 }
 const inSen = "Today is Monday";
 console.log(inSen);
 const res = resersWord(inSen);
 console.log(res);
---------------------------------------------------------------------------
function reverse (str) {
    var res = '';
    for (var i=str.length-1; i>=0; i--) {
      res += str[i];
  }
  return res;
}
console.log(reverse('pravinparandwal'));


Write a JavaScript function that takes an array of numbers and returns a new array with only the even numbers. 
Sample answer: By using the filter method on the array, I can check if each element is even or not by using the modulus operator (%) with 2. The element is even if the result is 0. This can be included in the new array. 
function filterEvenNumbers(numbers) { 
  return numbers.filter(num => num % 2 === 0); 
}
------------------------------------------------------------------------
let numbers = [10, 23, 12, 21];
let evenNo = [];
for (let i=0; i<numbers.length;i++) {
    if(numbers[i] % 2 === 0 )
    evenNo.push(numbers[i]);
}
console.log(`Even numbers in an array are: ${evenNo}`);
--------------------------------------------
let numbers = [10, 23, 12, 21, 86, 41, 55, 85, 90, 24];
// let evenNo = numbers.filter(function(item) {
//     return item % 2 === 0;
// })

let evenNo = numbers.filter(item =>  {
    return item % 2 === 0;
});
console.log(`Even numbers in an array are: ${evenNo}`);

Write a JavaScript program to find the largest element in a nested array. 
function findLargestElement(nestedArray) { 
  let largest = nestedArray[0][0]; 
  for (let arr of nestedArray) { 
    for (let num of arr) { 
      if (num > largest) { 
        largest = num; 
      } 
    } 
  } 
  return largest; 
}
---------------------------------------------------------------------------
const numbers = [
   34, 65, 67,
      [
         43, 76, 87, 23, 56, 7,
         [
            54, 7, 87, 23, 79, 994, 2
         ],
      54
   ], 54, 4, 2
];

const flat = numbers.flat();
const flat2 = flat.flat();
// const flat = [].concat(...numbers);
console.log(flat2);

const min = Math.min(...flat2);
const max = Math.max(...flat2);
console.log(min);
console.log(max);
------------------------------------------------------------------------------------
arr = [0, 1, 2, [3, 4]]
var res = [].concat.apply([], arr);
console.log(res);
let getGretest = (arr, gretest = -Infinity) => {
  for (let i=0; i< arr.length; i++) {
    if(Array.isArray(arr[i])) {
      return getGretest(arr[i], gretest);
    };
    if(arr[i] > gretest) {
      gretest = arr[i];
    }
  };
  return gretest;
};

console.log(getGretest(arr));

--------------------------------------------------------------------------------------
function findMaxFromNestedArray(arr) {
  let max = 0;
  for (let item of arr) {
    if(Array.isArray(item)) {
      let maxInChildArray = findMaxFromNestedArray(item);
      if (maxInChildArray > max) {
        max = maxInChildArray;
      }
    } else {
      if (item > max) {
        max = item;
      }
    }
  }
  
  return max;
}
console.log(findMaxFromNestedArray(arr))
Note: Array.isArray(item) // This method is useful for checking the type of a variable to ensure it is an array before performing array-specific operations on it.

Implement a function that checks if a given string is a palindrome (reads the same forwards and backwards) while ignoring whitespace and punctuation.
function isPalindrome(str) { 
  const cleanedStr = str.replace(/[^\w]/g, ”).toLowerCase(); 
  const reversedStr = cleanedStr.split(”).reverse().join(”); 
  return cleanedStr === reversedStr; 
} 

var words = ['foo', 'racecar', 'pineapple', 'porcupine', 'pineenip'];
var arr = [];
var str = words.slice(0);
var pal = str.toString().split("").reverse().join("").split(",");
console.log(pal);

for (let i = 0; i < words.length; i++) {
  for (let k = 0; k < pal.length; k++) {
    if (words[i] == pal[k]) {
      arr.push(words[i])
    }
  }
}

Implement a function that removes duplicates from an array, keeping only the unique elements. 
function removeDuplicates(arr) { 
  return arr.filter((item, index) => arr.indexOf(item) === index); 
} 
-------------------------------------------------------------------------
 
function removeDuplicates(arr) {
    return [...new Set(arr)];
}

const users=[
  {firstName:"john",lastName:"Biden",age:26},
  {firstName:"jimmy",lastName:"cob",age:75},
  {firstName:"sam",lastName:"lewis",age:50},
  {firstName:"Ronald",lastName:"Mathew",age:50},  
];

const ages = users.map(user => user.age);
const output = users.filter((user, index) => {
    return !ages.includes(user.age, index+1);;
});
-----------------------------------------------------
const ids = users.map(({title}) => title);
const output = users.filter(({title}, index) => 
  ids.includes(title, index +1));

Write a function that accepts a number and returns its factorial
let n = 4;
function factorial(n) { 
  if (n === 0 || n === 1) { 
    return 1; 
  } else { 
    return n * factorial( n - 1 );
  } 
} 
console.log(factorial(n));
-----------------------------------------------------------------------------
let n = 5;
function fact(n){
    let ans = 1;
    if(n===0) {
        return 1
    }
    for(let i=2; i<=n; i++){
        ans = ans * i;
    }
    return ans;
}
console.log(fact(n));
 
Write a function that takes an array of objects and a key, and returns a new array sorted based on the values of that key in ascending order.
function sortByKey(arr, key) { 
  return arr.sort((a, b) => a[key] – b[key]); 
} 
--------------------------------------------------------------------
var Arr = [1, 7, 2, 8, 3, 4, 5, 0, 9];

for (var i = 1; i < Arr.length; i++)
    for (var j = 0; j < i; j++)
        if (Arr[i] < Arr[j]) {
            let x = Arr[i];
            Arr[i] = Arr[j];
            Arr[j] = x;
        }

console.log(Arr);

Find all Palindrome Strings in given Array of strings
arr = ['abc', 'car', 'ada', 'racecar', 'cool']
function isPalindrome (str) {
    let res = str.split('').reverse().join('');
    return res == str;
}
function checkArr(arr) {
    let ans =[];
    
    for(let i=0; i<arr.length;i++) {
        if(isPalindrome(arr[i])) {
            ans.push(arr[i])
        }
    }
    return ans;
}
const finRes = checkArr(arr);
console.log(finRes);

Create a JavaScript function that returns the Fibonacci sequence up to a given number, utilizing memoization for optimized performance. 
function fibonacciWithMemoization(n) { 
  let memo = [0, 1]; 
  for (let i = 2; i <= n; i++) { 
    memo[i] = memo[i – 1] + memo[i – 2]; 
  } 
  return memo; 
} 
-------------------------------------------------------------------------------------
function fib(n) {
    let a=0, b=1, c, i;
  if(n==0) return a;
  for(i=2; i<=n; i++) {
      c=a+b;
      a=b;
      b=c;
  }
  return b;
}
Write a recursive function to calculate the factorial of a given number.
 function factorial(num) {
  if(num==0) {
    return 1;
  }
  return num*factorial(num -1);
}
console.log(factorial(3));

Implement a function that takes two sorted arrays and merges them into a single sorted array without using any built-in sorting functions.
function mergeArray(arr1, arr2) {
  // return [...arr1, ...arr2].sort((a,b) => a - b);
  let result = [];
  let i = 0, j = 0;
  while(i < arr1.length && j < arr2.length) {
    if(arr1[i] <= arr2[j]) {
      result.push(arr1[i]);
      i++;
    } else {
      result.push(arr2[j]);
      j++;
    }
  }
  // Add remaining elements from arr1
  while(i < arr1.length) {
    result.push(arr1[i]);
    i++;
  }
  // Add remaining elements from arr2
  while(j < arr2.length) {
    result.push(arr2[j]);
    j++;
  }
  return result;
}
let arr1 = [1, 3, 5];
let arr2 = [2, 4, 6];
console.log(mergeArray(arr1, arr2));
-----------------------------------------------------------------
function Numeric_sort(ar) {
    let i = 0, j;
    while (i < ar.length) {
        j = i + 1;
        while (j < ar.length) {

            if (ar[j] < ar[i]) {
                let temp = ar[i];
                ar[i] = ar[j];
                ar[j] = temp;
            }
            j++;
        }
        i++;
    }
}

let arr1 = [1, 3, 5];
let arr2 = [2, 4, 6];
let arr = [...arr1, ...arr2];
Numeric_sort(arr);
console.log(arr);

Write a function that returns the sum of all numbers in an array.
let myNums = [1, 2, 3, 4, 5];
let sum = 0;
for (let i=0; i < myNums.length ; i++) {
  sum += myNums[i];
}
console.log(sum);
---------------------------------------------------------------------
myNums.forEach(num => {
  sum += num; 
})
console.log(sum);
-----------------------------------------------------------------------
Calculating the sum of an array is using the reduce() method, which got introduced with ES6.
The reduce() method reduces all elements in an array into a single value.
let sum = myNums.reduce((total, num) => total + num, 0)
console.log(sum);
-------------------------------------------------------------------------
let abc = '12345'; // let is a string
let myfunc = num => Number(num);
let intArr = Array.from(String(abc), myfunc);

let sum = 0;
intArr.forEach(num => {
  sum += num;
})
console.log(intArr);
console.log(sum);

let inputArray = [
  {
    "geographyKey": 102,
    "geographyLevel": "Country",
    "geographyName": "United States",
    "isCohortCountry": false,
  },
  {
    "geographyKey": 102,
    "geographyLevel": "Country",
    "geographyName": "United States",
    "cohortKey": 238,
    "cohortName": "Cohort 1",
    "isCohortCountry": true
  },
   [{
    "geographyKey": 102,
    "geographyLevel": "Country",
    "geographyName": "United States",
    "cohortKey": 70,
    "cohortName": "Cohort 2",
    "isCohortCountry": true
  }],
  {
    "geographyKey": 156,
    "isCohortCountry": false,
    "geographyLevel": "Country",
    "geographyName": "Italy"
  },
  {
    "geographyKey": 156,
    "isCohortCountry": true,
    "geographyLevel": "Country",
    "geographyName": "Italy",
    "cohortKey": 238,
    "cohortName": "Cohort 1"
  },
  {
    "geographyKey": 156,
    "isCohortCountry": true,
    "geographyLevel": "Country",
    "geographyName": "Italy",
    "cohortKey": 70,
    "cohortName": "Cohort 2"
  }
];

const uniqueGrographic = inputArray
  .filter(item => !item.isCohortCountry)
  .map(item => ({
      geographyKey: item.geographyKey,
      geographyLevel: item.geographyLevel || item['geographyLevel'],
      geographyName: item.geographyName,
      isCohortCountry: item.isCohortCountry,
      cohortList: []
  }));
  
  
uniqueGrographic.forEach(geo => {
  inputArray
    .filter(item => item.isCohortCountry && item.geographyKey === geo.geographyKey)
    .forEach(cohort => {
      geo.cohortList.push({
        geographyKey: cohort.geographyKey,
        geographyLevel: cohort.geographyLevel || cohort['geographyLevel'],
        geographyName: cohort.geographyName,
        cohortKey: cohort.cohortKey,
        cohortName: cohort.cohortName,
        isCohortCountry: cohort.isCohortCountry
      });
    });
});
-----------------------------------------
Reduce
The callback argument is a function that will be called once for every item in the array. This function takes four arguments, but often only the first two are used.
accumulator - the returned value of the previous iteration
currentValue - the current item in the array
index - the index of the current item [optional]
array - the original array on which reduce was called [optional]
The initialValue argument is optional. If provided, it will be used as the initial accumulator value in the first call to the callback function.

const arr = [11,12,13,14,15];
const users=[
  {firstName:"john",lastName:"Biden",age:26},
  {firstName:"jimmy",lastName:"cob",age:75},
  {firstName:"sam",lastName:"lewis",age:50},
  {firstName:"Ronald",lastName:"Mathew",age:26},  
];
const output = arr.reduce((acc, curr) => {
  acc += curr;
  return acc;
});

const output = student.reduce((acc, curr) => {
  return acc+=curr.marks;
},0);
// 0 is a initial value of acc
const output = arr.reduce(function(acc, curr) {
  acc += curr;
  return acc;
});

const output = users.map((x) => {
  return x.firstName + ' ' + x.lastName;
});
var output = arr.filter((x) => {
  return x%2;
});

function isOdd(x) {
  return x%2;
}
var output = arr.filter(isOdd);

function double(x) {
  return x*2;
}
const output = arr.map(double);

const output = arr.map((x) => {
return x*2
});

const test = arr.reduce((acc, curr) => {
  if(acc[curr.age]) {
    acc[curr.age]++;
  } else {
    acc[curr.age]=1;
  }
  return acc;
},{})
// {} is the initial value for the accumulator acc. The function counts occurrences of each age in arr and stores these counts in acc.

const output = student.filter((x) => x.marks > 60 && x.rollNumber > 15);

const output = users
  .filter((x) => x.age > 30)
  .map((x) => x.firstName);

const numbers = [1, 2, 3, 4, 5]
const isEven = number => number % 2 === 0;
const isLessThanZero = number => number < 0;

//const output = numbers.filter(isEven);
// const output = numbers.every(isEven);
// const output = numbers.find(isEven)
//const output = numbers.findIndex(isEven) // same as indexOf, but searches in reverse.
// const output = numbers.indexOf(5)
// const output = numbers.lastIndexOf(2)
const output = numbers.some(isEven)

// Count string letters 
const countString = (str) => {
  const obj1 = {}, c=0
  for(let i=0; i<str.length; i++){
    if(!obj1[str[i]]){
      obj1[str[i]]=0;
    }
    obj1[str[i]]++
  }
  return obj1;
}
console.log(countString('users'));

Reverse an array without using reverse()
const numArray=[1, 2 ,3 ,4];
function reverseArray(arr) {
  const res = [];
  for(let i=numArray.length-1; i>=0; i--) {
    res.push(arr[i]);
  }
  return res;
}
console.log(reverseArray(numArray));

Print pattern: Right-aligned triangle of * of height n
function rightAlinedTriangle(n) {
  let res = "";
  for(let i=1; i<=n; i++) {
    res = ' '.repeat(n-i)+'*'.repeat(i);
    console.log(res);
  }
}
rightAlinedTriangle(5);

