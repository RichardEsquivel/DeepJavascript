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


