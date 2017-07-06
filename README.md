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
specify a property or element of an object or array
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

`arguments` is not really an array. It is an array-like object.`arguments` has a length property, but it lacks all of the array methods.

## Return
When a function is invoked, it begins execution with the first statement, and ends when it hits the } that closes the function body.

That causes the function to return control to the part of the program that invoked the function.

The return statement can be used to cause the function to return early. When return is executed, the function returns immediately without executing the remaining statements.

A function always returns a value. If the return value is not specified, then undefined is returned.

If the function was invoked with the new prefix and the return value is not an object, then this (the new object) is returned instead

## Exceptions
```js

	var add = function (a, b) {
		if (typeof a !== 'number' || typeof b !== 'number') {
			throw {
				name: 'TypeError',
				message: 'add needs numbers'
			};
		}
		return a + b;
	}

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

#6 Arrays
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

##Dimensions
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

Add Matix

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
