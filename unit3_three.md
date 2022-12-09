# What are all the JavaScript Data Types?
Number, String, Object, Boolean, Array, undefined, null

# What is the Difference Between Const Let and Var? Consider Scope ... Give an example
var: 
	- hoisted (always declared at top of scope, global if none)
    - function scope
let:
    - block scope
    - not redeclarable
const: 
    - block scope
    - not reassignable
    - not redeclarable

# Pass By Value vs Pass By Reference? Why would you say a String is pass by value/ or a value type? Why is an object a reference type?
A string is a pass by value type becuase the string is used as a specific peice of data, it can be modified but generally it is a self contained piece. An object is a reference type because the object holds key value pairs for multiple data points the user can pull.

# What do Map, Filter and Reduce do? Do they mutate the array you call them on?
The map() method is used for creating a new array from an existing one, applying a function to each one of the elements of the first array.

The filter() method takes each element in an array and it applies a conditional statement against it. If this conditional returns true, the element gets pushed to the output array. If the condition returns false, the element does not get pushed to the output array.

The reduce() method reduces an array of values down to just one value. To get the output value, it runs a reducer function on each element of the array.

# What are all the Falsey Values in JavaScript? Why do you think this is important to know?
A falsy value is something which evaluates to FALSE, for instance when checking a variable. There are only six falsey values in JavaScript: undefined , null , NaN , 0 , "" (empty string), and false of course.

# What are Async and Await?
Async and Await both are considered as special keywords which are provided by ES6 in order to perform some asynchronous data operations. Even synchronous operations could also be performed using these keywords.

# What is an async function?
The word “async” before a function means one simple thing: a function always returns a promise. Other values are wrapped in a resolved promise automatically.

# What are try and catch?
The try statement allows you to define a block of code to be tested for errors while it is being executed. The catch statement allows you to define a block of code to be executed, if an error occurs in the try block.
