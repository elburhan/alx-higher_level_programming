0x12 JavaScript - Warm Up
Introduction
This repository contains JavaScript scripts as part of a second chance project, initiated on Jan 8, 2024, and is expected to be completed by Jan 11, 2024.

General Information
JavaScript is a versatile language used for scripting and web front-end development. This project focuses on learning basic concepts through scripting before applying the knowledge to a dynamic AirBnB project using JavaScript and JQuery.

Tasks
First constant, first print

Write a script that prints "JavaScript is amazing."
Create a constant variable called myVar with the value "JavaScript is amazing."
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./0-javascript_is_amazing.js
JavaScript is amazing
3 languages

Write a script that prints three lines: "C is fun," "Python is cool," and "JavaScript is amazing."
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./1-multi_languages.js
C is fun
Python is cool
JavaScript is amazing
Arguments

Write a script that prints a message depending on the number of arguments passed.
If no arguments are passed, print "No argument."
If only one argument is passed, print "Argument found."
Otherwise, print "Arguments found."
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./2-arguments.js
No argument
$ ./2-arguments.js Best
Argument found
$ ./2-arguments.js Best School
Arguments found
Value of my argument

Write a script that prints the first argument passed to it.
If no arguments are passed, print "No argument."
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./3-value_argument.js
No argument
$ ./3-value_argument.js School
School
Create a sentence

Write a script that prints two arguments passed to it in the format: " is "
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./4-concat.js c cool
c is cool
$ ./4-concat.js c
c is undefined
$ ./4-concat.js
undefined is undefined
An Integer

Write a script that prints "My number: " followed by the first argument converted to an integer if possible.
If the argument can't be converted to an integer, print "Not a number."
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./5-to_integer.js
Not a number
$ ./5-to_integer.js 89
My number: 89
$ ./5-to_integer.js "89"
My number: 89
$ ./5-to_integer.js 89.89
My number: 89
$ ./5-to_integer.js School
Not a number
Loop to languages

Write a script that prints three lines using an array of strings and a loop.
The first line: "C is fun"
The second line: "Python is cool"
The third line: "JavaScript is amazing"
Use console.log(...) and a loop (while, for, etc.) to print the output.
Example:

bash
Copy code
$ ./6-multi_languages_loop.js
C is fun
Python is cool
JavaScript is amazing
I love C

Write a script that prints "C is fun" x times, where x is the first argument.
If no argument is passed, or the argument can't be converted to an integer, print "Missing number of occurrences."
Use console.log(...) and a loop (while, for, etc.) to print the output.
Example:

bash
Copy code
$ ./7-multi_c.js 2
C is fun
C is fun
$ ./7-multi_c.js 5
C is fun
C is fun
C is fun
C is fun
C is fun
$ ./7-multi_c.js
Missing number of occurrences
$ ./7-multi_c.js -3
Square

Write a script that prints a square using the character X.
The size of the square is determined by the first argument.
If the first argument can't be converted to an integer, print "Missing size."
Use console.log(...) and a loop (while, for, etc.) to print the output.
Example:

bash
Copy code
$ ./8-square.js
Missing size
$ ./8-square.js School
Missing size
$ ./8-square.js 2
XX
XX
$ ./8-square.js 6
XXXXXX
XXXXXX
XXXXXX
XXXXXX
XXXXXX
XXXXXX
$ ./8-square.js -3
Add

Write a script that prints the addition of two integers.
The first argument is the first integer, and the second argument is the second integer.
Define a function add(a, b) with the prototype function add(a, b).
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./9-add.js
NaN
$ ./9-add.js 1
NaN
$ ./9-add.js 1 7
8
$ ./9-add.js 13 89
102
Factorial

Write a script that computes and prints the factorial of an integer.
The first argument is an integer used for computing the factorial.
Factorial of NaN is 1.
Implement the factorial calculation recursively using a function.
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./10-factorial.js
1
$ ./10-factorial.js 3
6
$ ./10-factorial.js 89
1.6507955160908452e+136
$ ./10-factorial.js 333
Infinity
Second biggest!

Write a script that searches for the second biggest integer in the list of arguments.
If no argument is passed, print 0.
If the number of arguments is 1, print 0.
Use console.log(...) to print the output.
Example:

bash
Copy code
$ ./11-second_biggest.js
0
$ ./11-second_biggest.js 1
0
$ ./11-second_biggest.js 4 2 5 3 0 -3
4
Object

Update a script to replace the value 12 with 89 in an object.
Do not use var.
Example:

bash
Copy code
$ ./12-object.js
{ type: 'object', value: 12 }
{ type: 'object', value: 89 }
Add file

Write a function that returns the addition of two integers.
The function must be visible from outside.
The name of the function must be add.
Example:

bash
Copy code
$ cat 13-main.js
#!/usr/bin/node
const add = require('./13-add').add;
console.log(add(3, 5));
$ ./13-main.js
8
Const or not const

Write a file that modifies the value of myVar to 333.
The script is run with myVar = 89; before requiring the file.
Example:

bash
Copy code
$ cat 100-main.js
#!/usr/bin/node
myVar = 89;
require('./100-let_me_const');
console.log(myVar);
$ ./100-main.js
333
Call me Moby

Write a function that executes a given function x times.
The function must be visible from outside.
Prototype: function (x, theFunction)
Example:

bash
Copy code
$ cat 101-main.js
#!/usr/bin/node
const callMeMoby = require('./101-call_me_moby').callMeMoby;
callMeMoby(3, function () {
  console.log('C is fun');
});
$ ./101-main.js
C is fun
C is fun
C is fun
Add me maybe

Write a function that increments and calls a function.
The function must be visible from outside.
Prototype: function (number, theFunction)
Example:

bash
Copy code
$ cat 102-main.js
#!/usr/bin/node
const addMeMaybe = require('./102-add_me_maybe').addMeMaybe;
addMeMaybe(4, function (nb) {
  console.log('New value: ' + nb);
});
$ ./102-main.js
New value: 5
Increment object

Update a script by adding a new function incr that increments the integer value in an object.
Example:

bash
Copy code
$ cat 103-object_fct.js
#!/usr/bin/node
const myObject = {
  type: 'object',
  value: 12
};
console.log(myObject);
/*
YOUR CODE HERE
*/
myObject.incr();
console.log(myObject);
myObject.incr();
console.log(myObject);
myObject.incr();
console.log(myObject);
$ ./103-object_fct.js
{ type: 'object', value: 12 }
{ type: 'object', value: 13, incr: [Function] }
{ type: 'object', value: 14, incr: [Function] }
{ type: 'object', value: 15, incr: [Function
