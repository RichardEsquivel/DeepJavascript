Developing first commit for note taking

12.4.4.1 Runtime Semantics: Evaluation

Getify's Law's #17
When there's a divergence between what you think(brain) is happening in the code and what is actually being done by the computer that is when bugs enter the code.

The 3 Javascript Pillars
-Frameworks like React or Angular are still JS and based on same fundamental pillars, it turns out misunderstandings are often based on a misunderstanding of the pillars.

Pillars:

-TYPES, often avoided in JS thinking. Irresponsible to not understand this fact of the language
Primitive Types
Abstract Operations
Coercion
Equality
Typescript, Flow, etc.

"We should only use the triple === and who needs to care about types if we use that?"

-SCOPE
Nested Scope
Hoisting
Closure
Modules

-OBJECTS (ORIENTED), JS has an OBJECTS oriented system as opposed to Object which is Class based
*this
*class { }, should not be used in JS but should be learned and understood and if you must use it to understand how to use it well.
Prototypes
Closure
OO vs OOLO

Types
in JS NOT everything is an object but it can behave as an object
You can have something behave as an object in the code but that does not mean that it IS an object within your code.
According to the spec we have Undefined, Null, Boolean, String, Symbol, Number, and Object. These are the Primitve Types.

Undefined - has only one value that of undefined contained within it

String - primitive string not the string object that you can create "string" or 'string' literal for example

Number- refers to all of JS's numbers with one caveat

Boolean - refers to the specific true values true and false, older languages had only 0 and 1 to represent true and false whereas JS has actual values called true and false.

Object - this is a type and there are sub-types, and because there is boxing that can make things behave as an object.

X = 42 and X = "42" these are two different typed values and as a developer we are expecting two different things from these values as far as the behavior available to these two different types.

Accessing characters "42" vs the math that can be done on that type.

Sybmol a lesser known type that isn't widely used. Used to create pseud0- private keys on objects not really private but instead obscure. Possibly used more often in frameworks than in primitive code.

Undeclared? How are we dealing with things that aren't declared? The spec doesn't define it as a type but it does have a particular behavior to it that we can come to expect.

Null is defined as a type but is quirky. This is due to factors of a historical bug.

Function and Arrays are sub types of the Object type.
Function sub-type of Object, javascript doesn't list functions. Values listed as function have very different behavior differ from values that are per se numbers. JS refers to functions as callable options. A sub type of objects

Arrays, JS are subtypes of of the Object. A special type of object that has particular value and behavior.

BigInt, should be a primitive type soon in V8. BigInt supported in Node.

Unlike C++ and Java, in JS variables don't have a type but VALUES do. JS is a dynamically typed language. Type checking the process of verifying and enforcing the values of types. This can occur at compile time( a static check) or at run-time (dynamically checked)
Strongly typed languages require that when you declare a variable of a particular type it must stay of that type.
a = 50;
a= "50" would be illegal in that circumstance and throw an error and halt the operation of the compile.
A weakly typed language allows such type changes above and are perfectly legal.
Type checking is meant to confirm that we don't perform an action such as adding a number to a float or
a = "50" = 2

Static typing usually allows for compiled code that executes more quickly as since the compiler knows the exact data types that are being use this can result in machine code that uses less memory and performs faster. With dynamically typed variables are bound to objects at run time by means of assignment statements and it is possible to bind a variable objects of different types multiple times throughout the program. Errors appear at run time and not compile time and require more error checking. run time type information RTTI can allow late binding, there is no separate compilation step to wait on so you can debug a bit faster as errors appear during run time.

Value types
For example for type of v; statement we are not asking what is the type of variable v as a variable cannot have a type but was is the value type or type of the value that is in v!

when there is no value that value that you have is undefined. undefined indicates it does not currently have a value. You can have a variable that had a value and then was made undefined.

null is not an object, if you want to unset an object reference you use null but this is a bug.

typeof function will say function. we can use Array.isArray and other tools will help us distinguish further when needed.

BigInt can grow infinitely large up to the space of the memory in the system. not an i eee number like other numbers and they don't mix and match with other numbers.

-Undefined vs undeclared-

variable doesn't exist and will get back undefined when in reality that variable doesn't exist and it should have returned back undeclared. typeof is able to reference a thing that doesn't exist and not throw an error.

unitialized introduced with ES6 (aka TDZ) temporal dead zone. Certain variables like block scope never get initialized, three ways something can by empty in JS undefined exists but no value, undeclared do not exist, variable unitialized never get set to undefined. undefined initialized is undefined, never been initialized unitialized, never even created undeclared.

Special Values
NaN ("not a number") essentially it means sentinel value that means invalid number. Zero is not absense of numerical value in a programattic sense. NaN is the number that indicates it's not a valid number var myCatsAge = Number("n/a"); The myAge - "my son's age" turns that into NaN value, NaN equations equals NaN, myCatsAge === myCatsAge is NaN not equal. NaN does not have identity value of being equal to itself. undefined is equal to itself. undefined === undefined

isValue utility coerces things to numbers before it checks if it is NaN. isNaN("my son's age") it will coerce this string to the NaN value. Read spec and ES6 Number.isNaN does not do any coercion to a number first. NaN is an Invalid Number, the typeOf a NaN is a number it's just invalid. NaN results from a numeric operation that returns what is not a number. It is a numeric representation of an invalid number. If you want to return to someone that there is no valid number return NaN not -1. No valid number return NaN. Test for NaN appropriately.

Negative Zero exists in programming. IEEE 754, 0 with - on it.

Languages should do the correct thing and it is on developers to do what is reasonable to users.
.toString lies to us when doing -0, also trendRate = -0, trendRate === 0 is incorrect, < > also don't work to -0

Object.is(trendRate, -0); true
Object.is(trendRate, 0) false j Object.is is like a quadruple zero, can also check NaN with Object.is.

Mapping solution, -0 for directions can be useful, Math.sign returns, -0 can have uses such as based on trend values.

NaN value and -0 value.


Infinity is a built in constant in JS

Reviewing section for notes tomorow.