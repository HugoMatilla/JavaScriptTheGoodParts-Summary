<!-- TOC -->

- [2.Grammar](#2grammar)
  - [White Space](#white-space)
  - [Name](#name)
    - [Reserved Words](#reserved-words)
      - [Avoid also these ones](#avoid-also-these-ones)
      - [And these](#and-these)
  - [Numbers](#numbers)
  - [Strings](#strings)
  - [Statements](#statements)
    - [`var` Statements](#var-statements)
    - [Statements](#statements-1)
    - [Disruptive Statements](#disruptive-statements)
    - [Block](#block)
    - [If Statement](#if-statement)
    - [Swith Statements](#swith-statements)
    - [Case Clause](#case-clause)
    - [While Statement](#while-statement)
    - [For Statement](#for-statement)
    - [Do Statement](#do-statement)
    - [Try Statement](#try-statement)
    - [Throw Statement](#throw-statement)
    - [Return Statement](#return-statement)
    - [Break Statement](#break-statement)
    - [Expression Statement](#expression-statement)
  - [Expressions](#expressions)
    - [#Operands precedence](#operands-precedence)
    - [Prefix Operator](#prefix-operator)
    - [Infix operator](#infix-operator)
    - [Invoaction](#invoaction)
    - [Refinement](#refinement)
  - [Literals](#literals)
    - [Object Literal](#object-literal)
    - [Regex Literal](#regex-literal)
  - [Functions](#functions)
    - [Function Literal](#function-literal)
    - [Parameters](#parameters)
    - [Function body](#function-body)
- [3.Objects](#3objects)
  - [Object Literals](#object-literals)
  - [Retrieval](#retrieval)
  - [Update](#update)
  - [Reference](#reference)
  - [Prototype](#prototype)
  - [Reflection](#reflection)
  - [Enumeration](#enumeration)
  - [Delete](#delete)
  - [Global Abatement](#global-abatement)
- [4.Functions](#4functions)
  - [Function Objects](#function-objects)
  - [Function Literals](#function-literals)
  - [Invocation](#invocation)
    - [The Method Invocation Pattern](#the-method-invocation-pattern)
    - [The Function Invocation Pattern](#the-function-invocation-pattern)
    - [The Constructor Invocation Pattern](#the-constructor-invocation-pattern)
    - [The Apply Invocation Pattern](#the-apply-invocation-pattern)
    - [Arguments](#arguments)
  - [Return](#return)
  - [Exceptions](#exceptions)
  - [Augmenting Types](#augmenting-types)
  - [Recursion](#recursion)
  - [Scope](#scope)
  - [Closure](#closure)
  - [Callbacks](#callbacks)
  - [Module](#module)
  - [Cascade](#cascade)
  - [Curry](#curry)
  - [Memoization](#memoization)
- [5. Inheritance](#5-inheritance)
  - [Pseudo Classical](#pseudo-classical)
  - [Object Specifiers](#object-specifiers)
  - [Prototypal](#prototypal)
  - [Functional](#functional)
      - [Sample](#sample)
- [6 Arrays](#6-arrays)
  - [Array Literals](#array-literals)
  - [Length](#length)
  - [Delete](#delete-1)
  - [Enumeration](#enumeration-1)
  - [Confusion](#confusion)
  - [Methods](#methods)
  - [Dimensions](#dimensions)
- [8. Methods](#8-methods)
  - [Array](#array)
    - [`array.concat(item…)`](#arrayconcatitem)
    - [`array.join(separator)`](#arrayjoinseparator)
    - [`array.pop( )`](#arraypop-)
    - [`array.push(item…)`](#arraypushitem)
    - [`array.reverse( )`](#arrayreverse-)
    - [`array.shift( )`](#arrayshift-)
    - [`array.slice(start, end)`](#arrayslicestart-end)
    - [`array.sort(comparefn)`](#arraysortcomparefn)
    - [`array.splice(start, deleteCount, item…)`](#arraysplicestart-deletecount-item)
    - [`array.unshift(item…)`](#arrayunshiftitem)
  - [Function](#function)
    - [`function.apply(thisArg, argArray)`](#functionapplythisarg-argarray)
  - [Number](#number)
    - [`number.toExponential(fractionDigits)`](#numbertoexponentialfractiondigits)
    - [`number.toFixed(fractionDigits)`](#numbertofixedfractiondigits)
    - [`number.toPrecision(precision)`](#numbertoprecisionprecision)
    - [`number.toString(radix)`](#numbertostringradix)
  - [Object](#object)
    - [`object.hasOwnProperty(name)`](#objecthasownpropertyname)
  - [RegExp](#regexp)
    - [`regexp.exec(string)`](#regexpexecstring)
    - [```regexp.test(string)```](#regexpteststring)
  - [String](#string)
    - [`string.charAt(pos)`](#stringcharatpos)
    - [`string.charCodeAt(pos)`](#stringcharcodeatpos)
    - [`string.concat(string…)`](#stringconcatstring)
    - [`string.indexOf(searchString, position)`](#stringindexofsearchstring-position)
    - [`string.lastIndexOf(searchString, position)`](#stringlastindexofsearchstring-position)
    - [`string.localeCompare(that)`](#stringlocalecomparethat)
    - [`string.match(regexp)`](#stringmatchregexp)
    - [`string.replace(searchValue,replaceValue)`](#stringreplacesearchvaluereplacevalue)
    - [`string.search(regexp)`](#stringsearchregexp)
    - [`string.slice(start, end)`](#stringslicestart-end)
    - [`string.split(separator, limit)`](#stringsplitseparator-limit)
    - [`string.substring(start, end)`](#stringsubstringstart-end)
    - [`string.toLocaleLowerCase( )`](#stringtolocalelowercase-)
    - [`string.toLocaleUpperCase( )`](#stringtolocaleuppercase-)
    - [`string.toLowerCase( )`](#stringtolowercase-)
    - [`string.toUpperCase( )`](#stringtouppercase-)
    - [`String.fromCharCode(char…)`](#stringfromcharcodechar)
- [Awful Parts](#awful-parts)
  - [Global Variables](#global-variables)
  - [Scope](#scope-1)
  - [Semicolon Insertion](#semicolon-insertion)
  - [Reserved Words](#reserved-words-1)
  - [Unicode](#unicode)
  - [typeof](#typeof)
  - [parseInt](#parseint)
  - [+](#)
  - [Floating Point](#floating-point)
  - [NaN](#nan)
  - [Phony Arrays](#phony-arrays)
  - [Falsy Values](#falsy-values)
  - [hasOwnProperty](#hasownproperty-function hasOwnProperty() { [native code] }1)
  - [Object](#object-1)
- [Bad Parts](#bad-parts)
  - [==](#)
  - [`with` Statement](#with-statement)
  - [`eval`](#eval)
  - [`continue` Statement](#continue-statement)
  - [`switch` Fall Through](#switch-fall-through)
  - [Block-less Statements](#block-less-statements)
  - [`++` `--`](#---)
  - [Bitwise Operators](#bitwise-operators)
  - [The function Statement Versus the function Expression](#the-function-statement-versus-the-function-expression)
  - [Typed Wrappers](#typed-wrappers)
  - [`void`](#void)

<!-- /TOC -->
# 2.Grammar
## White Space
![alt text][space]
## Name
Names are used for statements, variables, parameters, property names, operators, and labels.
![alt text][name]

### Reserved Words
| 		   |            |            |              |
| -------- | ---------- | ---------- | ------------ |  
| abstract | else       | instanceof | super        |
| boolean  | enum       | int        | switch       |
| break    | export     | interface  | synchronized |
| byte     | extends    | let        | this         |
| case     | FALSE      | long       | throw        |
| catch    | final      | native     | throws       |
| char     | finally    | new        | transient    |
| class    | float      | null       | TRUE         |
| const    | for        | package    | try          |
| continue | function   | private    | typeof       |
| debugger | goto       | protected  | var          |
| default  | if         | public     | void         |
| delete   | implements | return     | volatile     |
| do       | import     | short      | while        |
| double   | in         | static     | with         |

#### Avoid also these ones

| 		             |                    |                |             
| ------------------ | ------------------ | -------------- |  
| alert              | frames             | outerHeight    |
| all                | frameRate          | outerWidth     |
| anchor             | function           | packages       |
| anchors            | getClass           | pageXOffset    |
| area               | hasOwnProperty     | pageYOffset    |
| Array              | hidden             | parent         |
| assign             | history            | parseFloat     |
| blur               | image              | parseInt       |
| button             | images             | password       |
| checkbox           | Infinity           | pkcs11         |
| clearInterval      | isFinite           | plugin         |
| clearTimeout       | isNaN              | prompt         |
| clientInformation  | isPrototypeOf      | propertyIsEnum |
| close              | java               | prototype      |
| closed             | JavaArray          | radio          |
| confirm            | JavaClass          | reset          |
| constructor        | JavaObject         | screenX        |
| crypto             | JavaPackage        | screenY        |
| Date               | innerHeight        | scroll         |
| decodeURI          | innerWidth         | secure         |
| decodeURIComponent | layer              | select         |
| defaultStatus      | layers             | self           |
| document           | length             | setInterval    |
| element            | link               | setTimeout     |
| elements           | location           | status         |
| embed              | Math               | String         |
| embeds             | mimeTypes          | submit         |
| encodeURI          | name               | taint          |
| encodeURIComponent | NaN                | text           |
| escape             | navigate           | textarea       |
| eval               | navigator          | top            |
| event              | Number             | toString       |
| fileUpload         | Object             | undefined      |
| focus              | offscreenBuffering | unescape       |
| form               | open               | untaint        |
| forms              | opener             | valueOf        |
| frame              | option             | window         |

#### And these

| 		         |            |             |             |
| -------------- | ---------- | ----------- | ----------- |  
| onbeforeunload | ondragdrop | onkeyup     | onmouseover |
| onblur         | onerror    | onload      | onmouseup   |
| ondragdrop     | onfocus    | onmousedown | onreset     |
| onclick        | onkeydown  | onmousemove | onsubmit    |
| oncontextmenu  | onkeypress | onmouseout  | onunload    |

## Numbers
Only one number type. 64-bit floating point. (Java double)

`NaN` is a number of an operation that cannot produce a normal result. Use `isNaN(number)` to detect it.

`Infinity` represents all values greater than `1.79769313486231570e+308`.

![alt text][numbers]
![alt text][integer]
![alt text][fraction]
![alt text][exponent]


## Strings
Strings can be wrapped in single quotes or double quotes.
The `\` (backslash) is the escape character.
Characters in JavaScript are 16 bits wide.

![alt text][string]

Escape sequences allow for inserting characters into strings that are not normally permitted
![alt text][escaped]

Strings have a `length` property

Strings are immutable.


## Statements
### `var` Statements
A compilation unit contains a set of executable statements.
![alt text][var]
### Statements
![alt text][statements]
### Disruptive Statements
![alt text][disruptive]
### Block
`Blocks` in JavaScript do not create a new scope, so variables should be defined at the top of the function, not in blocks.
![alt text][block]
### If Statement
![alt text][if]
False values: 
* `false`
* `null`
* `undefined`
* The empty string ''
* The number 0
* The number `NaN`
All other values are truthy, including true, the string 'false', and all objects.

### Swith Statements
![alt text][switch]
### Case Clause
![alt text][case]
### While Statement
![alt text][while]
### For Statement
![alt text][for]
### Do Statement
![alt text][do]
### Try Statement
![alt text][try]
### Throw Statement
![alt text][throw]
### Return Statement
![alt text][return]
### Break Statement
![alt text][break]
### Expression Statement
![alt text][expression-statement]

## Expressions
![alt text][expression]

The simplest expressions are:

* a literal value (such as a string or number)
* a variable
* a built-in value (true, false, null, undefined, NaN, or Infinity)
* an invocation expression preceded by new
* a refinement expression preceded by delete
* an expression wrapped in parentheses
* an expression preceded by a prefix operator
* an expression followed by:
	* An infix operator and another expression
	* The ? ternary operator followed by another expression, then by :, and then byyet another expression
	* An invocation
	* A refinement



### #Operands precedence
| . [] ( )  				  |  Refinement and invocation			 |
| delete new typeof + - ! 	  |  Unary operators					 |
| * / %  					  |  Multiplication, division, modulo	 |
| + -  						  |  Addition/concatenation, subtraction |
| >= <= > <  				  |  Inequality							 |
| === !==  					  |  Equality							 |
| &&  						  |  Logical and						 |
| ||  						  |  Logical or							 |
| ?: 						  |  Ternary							 |

### Prefix Operator

![alt text][prefix]

The values produced by typeof are 'number', 'string', 'boolean', 'undefined','function', and 'object'. If the operand is an array or null, then the result is 'object', which is wrong.

The + operator adds or concatenates. If you want it to add, make sure both operands are numbers.

The / operator can produce a noninteger result even if both operands are integers.

### Infix operator
![alt text][infix]

### Invoaction
Invocation causes the execution of a function value.
![alt text][invocation]

### Refinement
Specify a property or element of an object or array
![alt text][refinement]

## Literals
![alt text][literal]
### Object Literal
![alt text][object-literal]
### Regex Literal
![alt text][regexp-literal]


## Functions
### Function Literal
![alt text][function-literal]
A function literal defines a function value.

It can have an optional name that it can use to call itself recursively.

### Parameters
![alt text][parameters]
### Function body
![alt text][function-body]



# 3.Objects
Numbers, strings, and booleans are not objects the rest are.

Numbers, strings, and booleans are object-like in that they have methods, but they are immutable.

Objects in JavaScript are mutable keyed collections.

An object is a container of properties, where a property has a name and a value. 

* A property name can be any string, including the empty string.
* A property value can be any JavaScript value except for `undefined`.

Objects in JavaScript are class-free.

JavaScript includes a prototype linkage feature that allows one object to inherit the properties of another.

## Object Literals
An object literal is a pair of curly braces surrounding zero or more name/value pairs.

```js
	var empty_object = {};

	var stooge = {
		"first-name": "Jerome",
		"last-name": "Howard"
	};

```

## Retrieval
Values can be retrieved from an object by wrapping a string expression in a [ ] suffix.

Dot `.` notation can be use if the string expression is a constant, legal and not a reserved word.

`undefined` value is produced if an attempt is made to retrieve a nonexistent member.
```js
	stooge.middle-name //undefined

```

`||` can be used to fill default values

```js	
	var middle = stooge["middle-name"] || "(none)";

```

`&&` to avoid TypeError exception  when retrieving values from `undefined`
```js
	flight.equipment // undefined
	flight.equipment.model // throw "TypeError"
	flight.equipment && flight.equipment.model // undefined
```	

## Update
Updated by assignment. If exists it changes if not it is added.
```js
	stooge['first-name'] = 'Jerome';
```
## Reference
Objects are passed around by reference. They are never copied

## Prototype
Every object is linked to a prototype object from which it can inherit properties.

All Objects are linked to `Object.prototype`, an object that comes standard with JavaScript.

When you make a new object, you can select the object that should be its prototype.

## Reflection
Use `typeof` to determine what properties an object has.

`hasOwnProperty` method, which returns true if the object has a particular property. It does not look at the prototype chain

```js
	flight.hasOwnProperty('number') // true
	flight.hasOwnProperty('constructor') // false
```

## Enumeration
The for in statement can loop over all of the property names in an object, including functions and prototype properties that you might not be interested.

Filter them using `typeof`. The order will not be guaranteed 

```js
	var name;
	for (name in another_stooge) {
		if (typeof another_stooge[name] !== 'function') {
			document.writeln(name + ': ' + another_stooge[name]);
		}
	}
```
## Delete
`delete` removes a property from an object.

## Global Abatement
JavaScript makes it easy to define global variables but they weaken the resiliency of programs and should be avoided.

Create a single global variable for your application:
```js	
	var MYAPP = {};
	MYAPP.stooge = {
		"first-name": "Joe",
		"last-name": "Howard"
	};
	MYAPP.flight = {
		airline: "Oceanic",
		number: 815,
		...
	};
```	

By reducing your global footprint to a single name, you significantly reduce the chance of bad interactions with other applications, widgets, or libraries.


# 4.Functions
## Function Objects
* Functions are objects. 
* Objects are collections of name/value pairs.
* Objects have a hidden link to a prototype object.
* Objects produced from object literals are linked to Object.prototype.
* Function objects are linked to Function.prototype (which is linked to Object.prototype)
* Every function is created with two additional hidden properties: 
	*the function’s context 
	*the code that implements the function’s behavior.
* Every function object is created with a `prototype` property. Its value is an object with a `constructor` property whose value is the function. This is distinct from the hidden link to Function.prototype.
* Functions (because they are objects) can be:
	* stored in variables, objects, and arrays.
	* passed as arguments to functions 
	* returned from functions. 
	* have methods.

The special thing  about functions is that they can be invoked.

## Function Literals
Function objects are created with function literals:

```js
	var add = function (a, b) {
		return a + b;
	};
```

A function literal has four parts:

* 1. reserved word `function`.
* 2. The optional function’s name. If no name, it is called `anonymous function`.
* 3. Set of parameters wrapped in parentheses.
* 4. A set of statements wrapped in curly braces. These statements are the body of the function. They are executed when the function is invoked.

**Closure** A link to the outer function context.

## Invocation
Invoking a function suspends the execution of the current function, passing control and parameters to the new function. In addition to the declared parameters, every
function receives two additional parameters: `this` and `arguments`.

`this`:is determined by the invocation pattern.
There are four patterns of invocation in JavaScript:

* the method invocation pattern,
* the function invocation pattern,
* the constructor invocation pattern,
* the apply invocation pattern. 

The patterns differ in how the bonus parameter this is initialized.

### The Method Invocation Pattern
When a function is stored as a property of an object, we call it a method. 

When a method is invoked, this is bound to that object. 
If an invocation expression contains a refinement (that is, a . dot expression or [subscript] expression), it is
invoked as a method:

```js	
	myObject.increment(2);
```
The binding of `this` to the object happens at invocation time. 

Methods that get their object context from this are called public methods.
### The Function Invocation Pattern
When a function is not the property of an object, then it is invoked as a function:

```js
	var sum = add(3, 4); // sum is 7
```	
When a function is invoked with this pattern, `this` is bound to the global object. It should be to the outer function.

Defining a variable and assigns it the value of `this`  will make the trick.

By convention, the name of that variable is that:
```js	
	// Augment myObject with a double method.
	myObject.double = function ( ) {
		var that = this; // Workaround.
		var helper = function ( ) {
			that.value = add(that.value, that.value);
		};
		helper( ); // Invoke helper as a function.
	};
```	

### The Constructor Invocation Pattern
If a function is invoked with the new prefix, then a new object will be created with a hidden link to the value of the function’s prototype member, and this will be bound
to that new object.

Use of this style of constructor functions is not recommended.

```js
	var Quo = function (string) {
		this.status = string;
	}	
	
	Quo.prototype.get_status = function ( ) {
		return this.status;
	}

	var myQuo = new Quo("confused");
	document.writeln(myQuo.get_status( )); // confused

```

### The Apply Invocation Pattern
Functions can have methods.

The apply method lets us construct an array of arguments to use to invoke a function.

It also lets us choose the value of this. 

The apply method takes two parameters.

The first is the value that should be bound to this. 

The second is an array of parameters.

```js	
	var array = [3, 4];
	var sum = add.apply(null, array); // sum is 7
	
	var statusObject = {
		status: 'A-OK'
	};
	// statusObject does not inherit from Quo.prototype,
	// but we can invoke the get_status method on
	// statusObject even though statusObject does not have
	// a get_status method.
	var status = Quo.prototype.get_status.apply(statusObject);
	// status is 'A-OK'
```	

### Arguments
A bonus parameter that is available to functions when they are invoked is the arguments array. It gives the function access to all of the arguments that were supplied
with the invocation, including excess arguments that were not assigned to
parameters.
```js	
	var sum = function ( ) {
		var i, sum = 0;
		for (i = 0; i < arguments.length; i += 1) {
		sum += arguments[i];
	}
		return sum;
	};
	document.writeln(sum(4, 8, 15, 16, 23, 42)); // 108
```

`arguments` is not really an array. It is an array-like object.`arguments` has a length property, but it lacks all of the array methods.

## Return
When a function is invoked, it begins execution with the first statement, and ends when it hits the } that closes the function body.

That causes the function to return control to the part of the program that invoked the function.

The return statement can be used to cause the function to return early. When return is executed, the function returns immediately without executing the remaining statements.

A function always returns a value. If the return value is not specified, then undefined is returned.

If the function was invoked with the new prefix and the return value is not an object, then this (the new object) is returned instead

## Exceptions

```js	var add = function (a, b) {
		if (typeof a !== 'number' || typeof b !== 'number') {
			throw {
				name: 'TypeError',
				message: 'add needs numbers'
			};
		}
		return a + b;
	}
```
The throw statement interrupts execution of the function. 

It should be given an exception object containing a name and message.
 The exception object will be delivered to the catch clause of a try statement:

```js
	var try_it = function ( ) {
		try {
			add("seven");
		} catch (e) {
			document.writeln(e.name + ': ' + e.message);
		}
	}
	try_it( );
```
A try statement has a single catch block that will catch all exceptions. 

The exception handler will have to inspect the name to determine the type of the exception.

## Augmenting Types
JavaScript allows the basic types of the language to be augmented.


For example, by augmenting `Function.prototype`, we can make a method available to all functions:
```js
	Function.prototype.method = function (name, func) {
		this.prototype[name] = func;
		return this;
	};
```	

```js
	Number.method('integer', function ( ) {
		return Math[this < 0 ? 'ceiling' : 'floor'](this);
	});
	document.writeln((-10 / 3).integer( )); // -3
```
The prototypes of the basic types are public structures, so care must be taken when mixing libraries. One defensive technique is to add a method only if the method is
known to be missing:

```js
	Function.prototype.method = function (name, func) {
		if (!this.prototype[name]) {
		this.prototype[name] = func;
		}
	};
```

## Recursion
A recursive function is a function that calls itself, either directly or indirectly. 

Recursion is a powerful programming technique in which a problem is divided into a set of similar subproblems, each solved with a trivial solution.

## Scope
Scope in a programming language controls the visibility and lifetimes of variables and parameters.

```js
	var foo = function ( ) {
		var a = 3, b = 5;
		var bar = function ( ) {
	
			var b = 7, c = 11;
			// At this point, a is 3, b is 7, and c is 11
	
			a += b + c;
			// At this point, a is 21, b is 7, and c is 11
		};
		// At this point, a is 3, b is 5, and c is not defined
	
		bar( );
		// At this point, a is 21, b is 5
	};
```
JavaScript does not have block scope.

JavaScript does have function scope. The parameters and variables defined in a function are not visible outside of the function, and that a variable defined anywhere within a function is visible everywhere within the function

## Closure
The good news about scope is that inner functions get access to the parameters and variables of the functions they are defined within (with the exception of this and
arguments). This is a very good thing.

```js
	var quo = function (status) {
	  return {
	    get_status: function ( ) {
	      return status;
	    }
	  };
	};
	// Make an instance of quo.

	var myQuo = quo("amazed");

	console.log(myQuo.get_status( ));


```
When we call quo, it returns a new object containing a `get_status` method.

A reference to that object is stored in myQuo. 

The `get_status` method still has privileged access to quo’s `status` property even though quo has already returned.

`get_status` does not have access to a copy of the parameter; it has access to the parameter itself.

This is possible because the function has access to the context in which it was created. This is called **closure**.

## Callbacks
Functions can make it easier to deal with discontinuous events.

```js	
	request = prepare_the_request( );
	send_request_asynchronously(request, function (response) {
		display(response);
	});
```	
We pass a function parameter to the `send_request_asynchronously` function that will be called when the response is available.

## Module
A module is a function or object that presents an interface but that hides its state and implementation.

By using functions to produce modules, we can almost completely eliminate our use of global variables, thereby mitigating one of JavaScript’s worst features.

The module pattern takes advantage of function scope and closure to create relationships that are binding and private. In this example, only the deentityify method has access to the entity data structure.

The general pattern of a module is a function that defines private variables and functions; creates privileged functions which, through closure, will have access to the private variables and functions; and that returns the privileged functions or stores them in an accessible place.

Use of the module pattern can eliminate the use of global variables. It promotes information hiding and other good designs practices.

```js	
	var serial_maker = function ( ) {
		var prefix = '';
		var seq = 0;
		return {
			set_prefix: function (p) {
				prefix = String(p);
			},
			set_seq: function (s) {
				seq = s;
			},
			gensym: function ( ) {
				var result = prefix + seq;
				seq += 1;
				return result;
			}
		};
	};
	var seqer = serial_maker( );
	seqer.set_prefix = ('Q';)
	seqer.set_seq = (1000);
	var unique = seqer.gensym( ); // unique is "Q1000"
```

The methods do not make use of this or that. As a result, there is no way to compromise the `seqer`.

It isn’t possible to get or change the `prefix` or `seq` except as permitted by the methods. 

The seqer object is mutable, so the methods could be replaced, but that still does not give access to its secrets.

`seqer` is simply a collection of functions, and those functions are capabilities that grant specific powers to use or modify the secret state.

If we passed `seqer.gensym` to a third party’s function, that function would be able to generate unique strings, but would be unable to change the prefix or seq.


## Cascade
Some methods do not have a return value. 

If we have those methods return this instead of undefined, we can enable cascades.

```js
	getElement('myBoxDiv').
		move(350, 150).
		width(100).
		height(100).
		color('red').
		border('10px outset')
```	

## Curry
Functions are values, and we can manipulate function values in interesting ways.

Currying allows us to produce a new function by combining a function and an argument:

```js	
	var add1 = add.curry(1);
	document.writeln(add1(6)); //7
```

JavaScript does not have a curry method, but we can fix that by augmenting Function.prototype:
```js
	Function.method('curry', function ( ) {
		var slice = Array.prototype.slice,
		args = slice.apply(arguments),
		that = this;
		return function ( ) {
			return that.apply(null, args.concat(slice.apply(arguments)));
		};
	});
```

## Memoization
Functions can use objects to remember the results of previous operations, making it possible to avoid unnecessary work.

This optimization is called **memoization**.


We will keep our memoized results in a memo array that we can hide in a closure. 

When our function is called, it first looks to see if it already knows the result.

If it does, it can immediately return it:
```js
	var fibonacci = function ( ) {
		var memo = [0, 1];
		var fib = function (n) {
			var result = memo[n];
			if (typeof result !== 'number') {
				result = fib(n - 1) + fib(n - 2);
				memo[n] = result;
			}
			return result;
		};
		return fib;
	}( );
```

A generalized version:

```js	
	var memoizer = function (memo, fundamental) {
		var shell = function (n) {
			var result = memo[n];
			if (typeof result !== 'number') {
				result = fundamental(shell, n);
				memo[n] = result;
			}
			return result;
		};
	return shell;
	};	

```
```js
	var fibonacci = memoizer([0, 1], function (shell, n) {
		return shell(n - 1) + shell(n - 2);
	});
```

# 5. Inheritance 
In classical languages, objects are instances of classes, and a class can inherit from another class. JavaScript is a prototypal language, which means that objects inherit directly from other objects.

## Pseudo Classical
A much better alternative is to not use new at all.

The pseudoclassical form can provide comfort to programmers who are unfamiliar 

The classically inspired notation can induce programmers to compose hierarchies that are unnecessarily deep and complicated.

Much of the complexity of class hierarchies is motivated by the constraints of static type checking. JavaScript is completely free of those constraints.

## Object Specifiers
Use `makers` when having a lot of arguments in the constructor of an object.

So, instead of:
```js
	var myObject = maker(f, l, m, c, s);
```	

we can write:
```js
	var myObject = maker({
		first: f,
		last: l,
		state: s,
		city: c
	});
```

We could also use a JSON with all the parameters as the argument.

## Prototypal
Contrary to purely prototypal pattern, where we dispense with classes, in JavaScript we focus on the objects.

A new object can inherit the properties of an old object.

```js	
	var myMammal = {
		name : 'Herb the Mammal',
		get_name : function ( ) {
			return this.name;
		},
		says : function ( ) {
			return this.saying || '';
		}
	};
```
Using `create` from Chapter 3

```js
	var myCat = Object.create(myMammal);
	myCat.name = 'Henrietta';
	myCat.saying = 'meow';
	myCat.purr = function (n) {
		var i, s = '';
		for (i = 0; i < n; i += 1) {
			if (s) {
				s += '-';
			}
			s += 'r';
		}
		return s;
	};
	myCat.get_name = function ( ) {
		return this.says( ) + ' ' + this.name + ' ' + this.says( );
	};
```

This is differential inheritance. By customizing a new object, we specify the differences from the object on which it is based.

## Functional
One weakness of the inheritance patterns we have seen so far is that we get no privacy.

We make a function that will produce objects. It contains four steps:

1. It creates a new object. There are lots of ways to make an object.
2. It optionally defines private instance variables and methods. These are just ordinary vars of the function.
3. It augments that new object with methods. Those methods will have privileged access to the parameters and the vars defined in the second step.
4. It returns that new object.

```js
	var constructor = function (spec, my) {
		var that, other private instance variables;
		
		my = my || {};
		// Add shared variables and functions to my
		
		that = a new object;
		//Add privileged methods to that
		
		return that;
	};
```

1. The `spec` object contains all of the information that the constructor needs to make an instance.
2. The `my` object is a container of secrets that are shared by the constructors in the inheritance chain.
3. Declare the private instance variables and private methods for the object. This is done by simply declaring variables.
4. Add the shared secrets to the `my` object.
5. Make a new object and assign it to `that`.
6. Augment that, adding the privileged methods that make up the object’s interface.

```js
	var methodical = function ( ) {
		...
	};
	that.methodical = methodical;
```

7. Return `that`


#### Sample
The name and saying properties are now completely private. They are accessible only via the privileged get_name and says methods:

```js	
	var mammal = function (spec) {
		var that = {};
		that.get_name = function ( ) {
			return spec.name;
		};
		that.says = function ( ) {
			return spec.saying || '';
		};
		
		return that;
	};
	
	var myMammal = mammal({name: 'Herb'});
```

```js
	var cat = function (spec) {
		spec.saying = spec.saying || 'meow';
		var that = mammal(spec);
		
		that.purr = function (n) {
			return 'r'.repeat(n);
		};
		
		that.get_name = function ( ) {
			return that.says( ) + ' ' + spec.name + ' ' + that.says( );
		};
		
		return that;
	};
	
	var myCat = cat({name: 'Henrietta'});
```

The functional pattern also gives us a way to deal with super methods. 

Make a superior method that takes a method name and returns a function that invokes that method.

```js
	Object.method('superior', function (name) {
		var that = this,
		method = that[name];
		return function ( ) {
			return method.apply(that, arguments);
			};
	});
```

```js
	var coolcat = function (spec) {
		var that = cat(spec),
		super_get_name = that.superior('get_name');
		
		that.get_name = function (n) {
			return 'like ' + super_get_name( ) + ' baby';
		};

		return that;
	};

	var myCoolCat = coolcat({name: 'Bix'});
	var name = myCoolCat.get_name( );
	// 'like meow Bix meow baby'
```

The functional pattern has a great deal of flexibility. 

Gives us better encapsulation and information hiding and access to super methods.

# 6 Arrays
## Array Literals
Array literals provide a very convenient notation for creating new array values.

An array literal is a pair of square brackets surrounding zero or more values separated by commas.

Elements of an array are NOT required to be of the same type.

```js
	var empty = [];
	var numbers = [
		'zero', 'one', 'two', 'three', 'four',
		'five', 'six', 'seven', 'eight', 'nine'
	];
	empty[1] // undefined
	numbers[1] // 'one'
	empty.length // 0
	numbers.length // 10
	var misc = [
		'string', 98.6, true, false, null, undefined,
		['nested', 'array'], {object: true}, NaN];
```

## Length
Every array has a length property. 

JavaScript’s array length is not an upper bound. 

There is no array bounds error.

The length property is the largest integer property name in the array plus one. 

This is not necessarily the number of properties in the array:

```js	
	var myArray = [];
	myArray.length // 0
	myArray[1000000] = true;
	myArray.length // 1000001
	// myArray contains one property.
```	

The length can be set explicitly. 

Making the length larger does not allocate more space for the array. 

Making the length smaller will delete elements.

```js	
	numbers.length = 3;
	// numbers is ['zero', 'one', 'two']
```	

A new element can be appended to the end of an array by assigning to the array’s current length:
```js
	numbers[numbers.length] = 'shi';
	// numbers is ['zero', 'one', 'two', 'shi']
```	
Use push for that
```js	
	numbers.push('go');
	// numbers is ['zero', 'one', 'two', 'shi', 'go']
```

## Delete
Since JavaScript’s arrays are really objects, the delete operator can be used to remove elements from an array:

```js
	delete numbers[2];
	// numbers is ['zero', 'one', undefined, 'shi', 'go']
```

Unfortunately, that leaves a hole in the array. Arrays are objects, `indexes` ([1], [3]) are the `names` of the object. 

`array = {'0':'Peter', '1':'John'}` 

Names of the objects do not change after `delete`

Use `splice` for that.

```js	
	numbers.splice(2, 1);
	// numbers is ['zero', 'one', 'shi', 'go']
```
The second argument is the number of elements to delete.

Any additional arguments get inserted into the array at that point.	

## Enumeration	
Since JavaScript’s arrays are really objects, the `for in` statement can be used to iterate over all of the properties of an array.

Unfortunately, for in makes no guarantee about the order of the properties,

Use `for`  instead
```js
	for (var i = 0; i < myArray.length; i += 1) {
		document.writeln(myArray[i]);
	}	
```

## Confusion
When the property names are small sequential integers, you should use an array. Otherwise, use an object.

**NOTE:** `typeof` operator reports that the type of an array is 'object.

Use:
```js
	var is_array = function (value) {
		return Object.prototype.toString.apply(value) === '[object Array]';
	};
```
##Methods
JavaScript provides a set of methods for acting on arrays.

Array.prototype can be augmented as well.

Add the `reduce` method to arrays:

```js
	Array.method('reduce', function (f, value) {
		var i;
		for (i = 0; i < this.length; i += 1) {
			value = f(this[i], value);
		}
		return value;
	});
```

```js	
	var data = [4, 8, 10];

	var add = function (a, b) {
		return a + b;
	};

	var sum = data.reduce(add, 0); // sum is 22
```

We can also add methods directly to an individual array:

```js
	data.total = function ( ) {
		return this.reduce(add, 0);
	};
	total = data.total( ); // total is 22
	
```

Since the string 'total' is not an integer, adding a total property to an array does not change its `length`.

## Dimensions
Add array initializers

```js
	Array.dim = function (dimension, initial) {
		var a = [], i;
		for (i = 0; i < dimension; i += 1) {
			a[i] = initial;
		}
		return a;
	};
	// Make an array containing 10 zeros.
	var myArray = Array.dim(10, 0);
```

Add Matrix

```js
	Array.matrix = function (m, n, initial) {
		var a, i, j, mat = [];
	
		for (i = 0; i < m; i += 1) {
			a = [];
			for (j = 0; j < n; j += 1) {
				a[j] = initial;
			}
			mat[i] = a;
		}
	
		return mat;
	};

	// Make a 4 * 4 matrix filled with zeros.
	var myMatrix = Array.matrix(4, 4, 0);
```

#8. Methods

## Array
### `array.concat(item…)`
The concat method produces a **NEW** array containing a shallow copy of this array with the items appended to it.
```js	
	var a = ['a', 'b', 'c'];
	var b = ['x', 'y', 'z'];
	var c = a.concat(b, true);
	// c is ['a', 'b', 'c', 'x', 'y', 'z', true]
```

### `array.join(separator)`
The join method makes a string from an array.
```js	
	var a = ['a', 'b', 'c'];
	a.push('d');
	var c = a.join(''); // c is 'abcd';
```

### `array.pop( )`
The pop and push methods make an array work like a stack.
```js	
	var a = ['a', 'b', 'c'];
	var c = a.pop( ); // a is ['a', 'b'] & c is 'c'
```

### `array.push(item…)`
The push method appends items to the end of an array. Unlike the concat method, it **modifies**
the array and appends array items whole. It returns the new length:

```js	
	var a = ['a', 'b', 'c'];
	var b = ['x', 'y', 'z'];
	var c = a.push(b, true);
	// a is ['a', 'b', 'c', ['x', 'y', 'z'], true]
	// c is 5;
```	
	
### `array.reverse( )`
The reverse method modifies the array by reversing the order of the elements. 

It returns the array

```js	
	var a = ['a', 'b', 'c'];
	var b = a.reverse( );
	// both a and b are ['c', 'b', 'a']
```

### `array.shift( )`
The shift method removes the first element from an array and returns it.
Usually Slower than pop

```js	
	var a = ['a', 'b', 'c'];
	var c = a.shift( ); // a is ['b', 'c'] & c is 'a'
```

### `array.slice(start, end)`
The slice method makes a shallow copy of a portion of an array. 
```js	
	var a = ['a', 'b', 'c'];
	var b = a.slice(0, 1); // b is ['a']
	var c = a.slice(1); // c is ['b', 'c']
	var d = a.slice(1, 2); // d is ['b']
```
### `array.sort(comparefn)`
The sort method sorts the contents of an array in place. 

It sorts arrays of numbers incorrectly:
```js 
  var n = [4, 8, 15, 16, 23, 42];
  n.sort( );
  // n is [15, 16, 23, 4, 42, 8]
```
You may replace the comparison function with your own. 

Your comparison function should take two parameters and return 0 if the two parameters are equal, a negative number if the first parameter should come first, and a positive number if the second parameter should come first.

```js
  n.sort(function (a, b) {
  return a - b;
  });
  // n is [4, 8, 15, 16, 23, 42];
```

### `array.splice(start, deleteCount, item…)`

The splice method removes elements from an array, replacing them with new items.

```js
  var a = ['a', 'b', 'c'];
  var r = a.splice(1, 1, 'ache', 'bug');
  // a is ['a', 'ache', 'bug', 'c']
  // r is ['b']
```

### `array.unshift(item…)`
The unshift method is like the push method except that it shoves the items onto the front of this array instead of at the end.

It returns the array’s new length:

```js
  var a = ['a', 'b', 'c'];
  var r = a.unshift('?', '@');
  // a is ['?', '@', 'a', 'b', 'c']
  // r is 5
``` 

## Function
### `function.apply(thisArg, argArray)`
The apply method invokes a function, passing in the object that will be bound to this and an optional array of arguments. 

The apply method is used in the [The Apply Invocation Pattern](#the-apply-invocation-pattern)

## Number
### `number.toExponential(fractionDigits)`
The `toExponential` method converts this number to a string in the exponential form. 

The optional fractionDigits parameter controls the number of decimal places. 

It should be between 0 and 20:

```js
  document.writeln(Math.PI.toExponential(0));  // 3e+0
  document.writeln(Math.PI.toExponential(2));  // 3.14e+0
  document.writeln(Math.PI.toExponential(7));  // 3.1415927e+0
  document.writeln(Math.PI.toExponential(16)); // 3.1415926535897930e+0
  document.writeln(Math.PI.toExponential( ));  // 3.141592653589793e+0
```

### `number.toFixed(fractionDigits)`
The `toFixed` method converts this number to a string in the decimal form. 

The optional fractionDigits parameter controls the number of decimal places. 

It should be between 0 and 20. The default is 0:
```js
  document.writeln(Math.PI.toFixed(0));  // 3
  document.writeln(Math.PI.toFixed(2));  // 3.14
  document.writeln(Math.PI.toFixed(7));  // 3.1415927
  document.writeln(Math.PI.toFixed(16)); // 3.1415926535897930
  document.writeln(Math.PI.toFixed( ));  // 3
```
### `number.toPrecision(precision)`
The `toPrecision` method converts this number to a string in the decimal form.

The optional precision parameter controls the number of digits of precision. 

It should be between 1 and 21:
```js
  document.writeln(Math.PI.toPrecision(2));  // 3.1
  document.writeln(Math.PI.toPrecision(7));  // 3.141593
  document.writeln(Math.PI.toPrecision(16)); // 3.141592653589793
  document.writeln(Math.PI.toPrecision( ));  // 3.141592653589793
```  

### `number.toString(radix)`
The `toString` method converts this number to a string. 

The optional radix parameter controls radix, or base. 

It should be between 2 and 36.

The default radix is base 10.

The radix parameter is most commonly used with integers, but it can be used on any number.

```js
document.writeln(Math.PI.toString(2));  // 11.001001000011111101101010100010001000010110100011
document.writeln(Math.PI.toString(8));  // 3.1103755242102643
document.writeln(Math.PI.toString(16)); // 3.243f6a8885a3
document.writeln(Math.PI.toString( ));  // 3.141592653589793
```

## Object
### `object.hasOwnProperty(name)`
The `hasOwnProperty` method returns true if the object contains a property having the name.

The prototype chain is not examined.

This method is useless if the name is hasOwnProperty

```js
var a = {member: true};
var b = Object.create(a); // from Chapter 3
var t = a.hasOwnProperty('member'); // t is true
var u = b.hasOwnProperty('member'); // u is false
var v = b.member; // v is true
```

## RegExp
### `regexp.exec(string)`
The exec method is the most powerful (and slowest) of the methods that use regular expressions.

If it successfully matches the regexp and the string, it returns an array.

The 0 element of the array will contain the substring that matched the regexp. 

The 1 element is the text captured by group 1, the 2 element is the text captured by group 2, and so on. 

If the match fails, it returns null.

### ```regexp.test(string)```
The test method is the simplest (and fastest) of the methods that use regular expressions.

If the regexp matches the string, it returns true; otherwise, it returns false. 

Do not use the `g` flag with this method:

```js
var b = /&.+;/.test('frank &amp; beans');
// b is true
```
## String
### `string.charAt(pos)`
The `charAt` method returns the character at position pos in this string. 

If pos is less than zero or greater than or equal to `string.length`, it returns the empty string. 

```js
var name = 'Curly';
var initial = name.charAt(0); // initial is 'C'
```

### `string.charCodeAt(pos)`
The `charCodeAt` method is the same as `charAt` except that instead of returning a string, it returns an integer representation of the code point value of the character at position `pos` in
that string.

If `pos` is less than zero or greater than or equal to `string.length`, it returns NaN

```js
var name = 'Curly';
var initial = name.charCodeAt(0); // initial is 67
```
### `string.concat(string…)`
The `concat` method makes a new string by concatenating other strings together. 

It is rarely used because the + operator is more convenient:
```js
var s = 'C'.concat('a', 't'); // s is 'Cat'
```

### `string.indexOf(searchString, position)`
The `indexOf` method searches for a searchString within a string. 

If it is found, it returns the position of the first matched character;otherwise, it returns –1. 

The optional position parameter causes the search to begin at some specified position in the `string`

```js
var text = 'Mississippi';
var p = text.indexOf('ss'); // p is 2
p = text.indexOf('ss', 3); // p is 5
p = text.indexOf('ss', 6); // p is -1
```
### `string.lastIndexOf(searchString, position)`
The `lastIndexOf` method is like the `indexOf` method, except that it searches from the end of the string instead of the front:

```js
var text = 'Mississippi';
var p = text.lastIndexOf('ss'); // p is 5
p = text.lastIndexOf('ss', 3); // p is 2
p = text.lastIndexOf('ss', 6); // p is 5
```

### `string.localeCompare(that)`
The `localCompare` method compares two strings.

The rules for how the strings are compared are not specified.

If this string is less than that string, the result is negative. 

If they are equal, the result is zero. 

This is similar to the convention for the `array.sort` comparison function:
```js
var m = ['AAA', 'A', 'aa', 'a', 'Aa', 'aaa'];
m.sort(function (a, b) {
return a.localeCompare(b);
});
// m (in some locale) is
// ['a', 'A', 'aa', 'Aa', 'aaa', 'AAA']
```
### `string.match(regexp)`
The match method matches a string and a regular expression. 

How it does this depends on the `g` flag. 

If there is no g flag, then the result of calling `string.match(regexp)` is the same as calling `regexp.exec(string)`.

However, if the regexp has the `g` flag, then it produces an array of all the matches but excludes the capturing groups.

```js
var text = '<html><body bgcolor=linen><p>' +
'This is <b>bold<\/b>!<\/p><\/body><\/html>';
var tags = /[^<>]+|<(\/?)([A-Za-z]+)([^<>]*)>/g;
var a, i;
a = text.match(tags);
for (i = 0; i < a.length; i += 1) {
document.writeln(('// [' + i + '] ' + a[i]).entityify( ));
}
// The result is
// [0] <html>
// [1] <body bgcolor=linen>
// [2] <p>
// [3] This is
// [4] <b>
// [5] bold
// [6] </b>
// [7] !
// [8] </p>
// [9] </body>
// [10] </html>
```

### `string.replace(searchValue,replaceValue)`
The `replace` method does a search and replace operation on this string, producing a new string.

The searchValue argument can be a string or a regular expression object. 

If it is a string, only the first occurrence of the searchValue is replaced

```js
var result = "mother_in_law".replace('_', '-');
```
will produce "mother-in_law", which might be a disappointment.

If searchValue is a regular expression and if it has the `g` flag, then it will replace all occurrences.

If it does not have the `g` flag, then it will replace only the first  ccurrence.

The replaceValue can be a string or a function.

|Dollar sequence |  Replacement |
|----------------|----------------------------|
| $$             | $                          |
| $&             | The matched text           |
| $ number       | Capture group text         |
| $`             |The text preceding the match|
| $'             |The text following the match|

If the replaceValue is a function, it will be called for each match, and the string returned by the function will be used as the replacement text. 

The first parameter passed to the function is the matched text.

### `string.search(regexp)`
The `search` method is like the indexOf method, except that it takes a regular expression object instead of a string.

The g flag is ignored. 
```js
var text = 'and in it he says "Any damn fool could';
var pos = text.search(/["']/); // pos is 18
```
### `string.slice(start, end)`
The `slice` method makes a new string by copying a portion of another string. 

If the start parameter is negative, it adds `string.length` to it.

The end parameter is optional, and its default value is `string.length`.

If the end parameter is negative, then string.length is added to it.

The end parameter is one greater than the position of the last character. 

```js
var text = 'and in it he says "Any damn fool could';
var a = text.slice(18);
// a is '"Any damn fool could'
var b = text.slice(0, 3);
// b is 'and'
var c = text.slice(-5);
// c is 'could'
var d = text.slice(19, 32);
// d is 'Any damn fool'
```
### `string.split(separator, limit)`
The `split` method creates an array of strings by splitting this string into pieces. 

The optional limit parameter can limit the number of pieces that will be split.

The separator parameter can be a string or a regular expression.

If the separator is the empty string, an array of single characters is produced:
```js
var digits = '0123456789';
var a = digits.split('', 5);
// a is ['0', '1', '2', '3', '456789']
```
Otherwise, the string is searched for all occurrences of the separator.

Each unit of text between the separators is copied into the array. 

The `g` flag is ignored:

```js
var ip = '192.168.1.0';
var b = ip.split('.');
// b is ['192', '168', '1', '0']
var c = '|a|b|c|'.split('|');
// c is ['', 'a', 'b', 'c', '']
```

### `string.substring(start, end)`
The `substring` method is the same as the slice method except that it doesn’t handle the
adjustment for negative parameters.

There is no reason to use the substring method. Use slice instead.

### `string.toLocaleLowerCase( )`

The `toLocaleLowerCase` method produces a new string that is made by converting this
string to lowercase using the rules for the locale. 

This is primarily for the benefit of Turkish because in that language ‘I’ converts to ı, not ‘i’.

### `string.toLocaleUpperCase( )`
The `toLocaleUpperCase` method produces a new string that is made by converting this
string to uppercase using the rules for the locale. 

This is primarily for the benefit of Turkish, because in that language ‘i’ converts to ‘ ’, not ‘I’.

### `string.toLowerCase( )`
The `toLowerCase` method produces a new string that is made by converting this string to
lowercase.

### `string.toUpperCase( )`
The `toUpperCase` method produces a new string that is made by converting this string to
uppercase.
### `String.fromCharCode(char…)`

The `String.fromCharCode` function produces a string from a series of numbers.
```js
var a = String.fromCharCode(67, 97, 116);
// a is 'Cat'
```

# Awful Parts
## Global Variables
A global variable is a variable that is visible in every scope.

Because a global variable can be changed by any part of the program at any time, they can significantly complicate the behavior of the program.

There are three ways to define global variables. 

1. Place a var statement outside of any function:
```js 
var foo = value;
```

2. Add a property directly to the global object. ie:
```js
window.foo = value;
```

3. Use a variable without declaring it.
```js
foo = value;
```
JavaScript’s policy of making forgotten variables global creates bugs that can be very difficult to find.

## Scope
JavaScript uses the block syntax, but does not provide block scope: 

_A variable declared in a block is visible everywhere in the function containing the block._

Best practice is to declare all variables at the top of each function.

## Semicolon Insertion
JavaScript has a mechanism that tries to correct faulty programs by automatically inserting semicolons.

Do not depend on this. It can mask more serious errors.

```js
return
{
  status: true
};
// returns undefined
```

```js
return {
  status: true
};
//returns an object
```

## Reserved Words
The following words are reserved in JavaScript:

`abstract boolean break byte case catch char class const continue debugger default
delete do double else enum export extends false final finally float for function goto
if implements import in instanceof int interface long native new null package private
protected public return short static super switch synchronized this throw throws
transient true try typeof var volatile void while with`

They cannot be used to name variables or parameters.

When reserved words are used as keys in object literals, they must be quoted.

They cannot be used with the dot notation, so it is sometimes necessary to use the bracket notation instead.

```js
var method; // ok
var class; // illegal
object = {box: value}; // ok
object = {case: value}; // illegal
object = {'case': value}; // ok
object.box = value; // ok
object.case = value; // illegal
object['case'] = value; // ok
```

## Unicode
JavaScript’s characters are 16 bits. That is enough to cover the original 65,536 (which is now known as the Basic Multilingual Plane).

Each of the remaining million characters can be represented as a pair of characters.

Unicode considers the pair to be a single character. 

JavaScript thinks the pair is two distinct characters.

## typeof
```js
typeof null
```
returns `object`

You can fix it with:
```js
if (my_value && typeof my_value === 'object') {
  // my_value is an object or an array!
}
```

Some implementations report that:
```js
typeof /a/
```
is `object`, and others say that it is `function`.

## parseInt
`parseInt` is a function that converts a string into an integer.

`parseInt("16")` and `parseInt("16 tons")` produce the same result.

If the first character of the string is 0, then the string is evaluated in base 8 instead of
base 10.

`parseInt("08")` and `parseInt("09")` produce 0 as their result.

Fortunately, `parseInt` can take a `radix` parameter, so that `parseInt("08",10)` produces 8.

Use always the **radix**

## +
The + operator can add or concatenate.

Which one it does depends on the types of the parameters.

If either operand is an empty string, it produces the other operand
converted to a string.

If both operands are numbers, it produces the sum. 

Otherwise, it converts both operands to strings and concatenates them.


## Floating Point
Binary floating-point numbers are inept at handling decimal fractions, so 0.1 + 0.2 is not equal to 0.3.

Use Integer aritmetic. ie: 1.05$ = 105/100 $

## NaN
The value NaN is a special quantity defined by IEEE 754. It stands for not a number, even though:
```js
typeof NaN === 'number' // true
```
The value can be produced by attempting to convert a string to a number when the string is not in the form of a number. For example:
```js
+ '0' // 0
+ 'oops' // NaN
```

`NaN` is not equal to itself.
```js
NaN === NaN // false
NaN !== NaN // true
```
`isNaN` function that can distinguish between numbers and `NaN`:
```js
isNaN(NaN) // true
isNaN(0) // false
isNaN('oops') // true
isNaN('0') // false
```

You may want to define your own isNumber function:
```js
var isNumber = function isNumber(value) { 
  return typeof value === 'number' && isFinite(value);
}
```
## Phony Arrays
Javascript arrays can be considerably worse than real arrays

The typeof operator does not distinguish between arrays and objects. You need
```js
if (my_value && typeof my_value === 'object' && typeof my_value.length === 'number' && !(my_value.propertyIsEnumerable('length')) {
  // my_value is truly an array!
}
```
In any case, the test can still fail if the propertyIsEnumerable method is overridden.

## Falsy Values
JavaScript has a surprisingly large set of falsy values

|Value| Type |
| --- | ----  |
|0| Number|
|NaN (not a number)| Number|
|'' (empty string) |String|
|false| Boolean|
|null| Object|
|undefined| Undefined|

## hasOwnProperty
Unfortunately, `hasOwnProperty` is a method, not an operator, so in any object it could be replaced.

## Object
JavaScript’s objects are never truly empty because they can pick up members from the prototype chain. 

And sometimes that matters.

# Bad Parts
## ==
Use always `===` and `!==` instead.

```js
'' == '0' // false
0 == '' // true
0 == '0' // true
false == 'false' // false
false == '0' // true
false == undefined // false
false == null // false
null == undefined // true
' \t\r\n ' == 0 // true
```

## `with` Statement
the `with` statement was intended to provide a shorthand when
accessing the properties of an object.

Unfortunately, its results can sometimes be unpredictable, so it should be avoided.

## `eval`
The eval function passes a string to the JavaScript compiler and executes the result.

Should be avoided as `setInterval`, `setTimeout` and the Function constructor

## `continue` Statement
The continue statement jumps to the top of the loop.

## `switch` Fall Through
The switch statement was modeled after the FORTRAN IV computed go to statement.

Each case falls through into the next case unless you explicitly disrupt the flow

## Block-less Statements
An if or while or do or for statement can take a block or a single statement.

```js
if (ok)
  t = true;
//can become:
if (ok)
  t = true;
  advance( );
//which looks like:
if (ok) {
  t = true;
  advance( );
}
//but which actually means:
if (ok) {
  t = true;
}
advance( );
```

## `++` `--`
When `++` and `--` are used , the code tended to be too
tight, too tricky, too cryptic. 

Don’t use them

## Bitwise Operators
JavaScript has the same set of bitwise operators as Java:
```js
& and
| or
^ xor
~ not
>> signed right shift
>>> unsigned right shift
<< left shift
```
Bitwise operators convert their number operands into integers, do their business, and then convert them back.

They are slow

## The function Statement Versus the function Expression
The statement:
```js
function foo( ) {}
```
means about the same thing as:
```js
var foo = function foo( ) {};
```

`function` statements are subject to _hoisting_. This means that regardless of where a `function` is placed, it is moved to the top of the scope in which it is defined.

The first thing in a statement cannot be a function expression because the official grammar assumes that a statement that starts with the word function is a function statement.

The workaround is to wrap the function expression in parentheses:
```js
(function ( ) {
  var hidden_variable;
  // This function can have some impact on
  // the environment, but introduces no new
  // global variables.
})(); 
```

## Typed Wrappers
JavaScript has a set of typed wrappers. For example:

```js
new Boolean(false)
```

Don’t use `new Boolean` or `new Number` or `new String`.

Also avoid `new Object` and `new Array`. Use `{}` and `[]` instead

`new`
JavaScript’s new operator creates a new object that inherits from the operand’s prototype
member, and then calls the operand, binding the new object to this. This gives
the operand (which had better be a constructor function) a chance to customize the
new object before it is returned to the requestor.

If youforget to use the new operator, youinstead get an ordinary function call, and
this is bound to the global object instead of to a new object. That means that your
function will be clobbering global variables when it attempts to initialize the new
members.

Not use `new` at all.

## `void`
`void` is an operator that takes an operand and returns `undefined`.

This is not useful, and it is very confusing.

Avoid void.

[block]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad02.png
[break]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad03.png
[case]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad04.png
[disruptive]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad05.png
[do]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad06.png
[escaped]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad07.png
[exponent]:  http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad08.png
[expression]:http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad09.png
[expression-statement]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad10.png
[function-body]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad13.png
[function-literal]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad14.png
[if]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad15.png
[infix]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad16.png
[invocation]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad18.png
[integer]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad17.png
[fraction]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad12.png 
[for]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad11.png
[literal]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad19.png
[name]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad20.png
[numbers]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad21.png
[object-literal]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad22.png
[parameters]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad23.png
[prefix]:http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad24.png
[refinement]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad25.png
[regexp-literal]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad32.png
[return]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad35.png
[space]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad43.png
[string]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad37.png
[statements]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad36.png
[switch]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad38.png
[throw]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad39.png
[try]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad40.png
[var]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad41.png
[while]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad42.png

[regexp1]: http://cdn.oreilly.com/excerpts/9780596517748/web/jsgp_ad26.png
