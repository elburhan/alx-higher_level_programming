# alx-higher_level_programming

This repository contains JavaScript code for different tasks related to objects, scopes, and closures.

## Table of Contents

- [0. Rectangle](#0-rectangle)
- [1. Rectangle #1](#1-rectangle-1)
- [2. Rectangle #2](#2-rectangle-2)
- [3. Rectangle #3](#3-rectangle-3)
- [4. Rectangle #4](#4-rectangle-4)
- [5. Square #0](#5-square-0)
- [6. Square #1](#6-square-1)
- [7. Occurrences](#7-occurrences)
- [8. Esrever](#8-esrever)
- [9. Log me](#9-log-me)
- [10. Number conversion](#10-number-conversion)
- [11. Factor index](#11-factor-index)
- [12. Sorted occurrences](#12-sorted-occurrences)
- [13. Concat files](#13-concat-files)

## 0. Rectangle

- File: 0-rectangle.js
- Description: Write an empty class Rectangle that defines a rectangle. You must use the class notation for defining your class.

```javascript
const Rectangle = require('./0-rectangle');

const r1 = new Rectangle();
console.log(r1);
console.log(r1.constructor);
1. Rectangle #1
File: 1-rectangle.js
Description: Write a class Rectangle that defines a rectangle. You must use the class notation for defining your class. The constructor must take 2 arguments w and h, initializing the instance attribute width with the value of w, and height with the value of h.
javascript
Copy code
const Rectangle = require('./1-rectangle');

const r1 = new Rectangle(2, 3);
console.log(r1);
console.log(r1.width);
console.log(r1.height);
2. Rectangle #2
File: 2-rectangle.js
Description: Write a class Rectangle that defines a rectangle. You must use the class notation for defining your class. The constructor must take 2 arguments w and h, initializing the instance attribute width with the value of w, and height with the value of h. If w or h is equal to 0 or not a positive integer, create an empty object.
javascript
Copy code
const Rectangle = require('./2-rectangle');

const r1 = new Rectangle(2, 3);
console.log(r1);
console.log(r1.width);
console.log(r1.height);

const r2 = new Rectangle(2, -3);
console.log(r2);
console.log(r2.width);
console.log(r2.height);
...

Continue providing similar information for each task.

License
This project is licensed under the MIT License - see the LICENSE file for details.

sql
Copy code

Remember to replace the placeholders with actual details, and add any specific instructions or information related to your project.
User
provide the info for the rest of the tasks
ChatGPT
Certainly! Here is the continuation of the README.md file for the remaining tasks:

markdown
Copy code
...

## 3. Rectangle #3

- File: 3-rectangle.js
- Description: Write a class Rectangle that defines a rectangle. You must use the class notation for defining your class. The constructor must take 2 arguments w and h, initializing the instance attribute width with the value of w, and height with the value of h. If w or h is equal to 0 or not a positive integer, create an empty object. Create an instance method called print() that prints the rectangle using the character X.

```javascript
const Rectangle = require('./3-rectangle');

const r1 = new Rectangle(2, 3);
r1.print();

const r2 = new Rectangle(10, 5);
r2.print();
4. Rectangle #4
File: 4-rectangle.js
Description: Write a class Rectangle that defines a rectangle. You must use the class notation for defining your class. The constructor must take 2 arguments w and h, initializing the instance attribute width with the value of w, and height with the value of h. If w or h is equal to 0 or not a positive integer, create an empty object. Create an instance method called print() that prints the rectangle using the character X. Create instance methods called rotate() that exchanges the width and the height of the rectangle, and double() that multiplies the width and the height of the rectangle by 2.
javascript
Copy code
const Rectangle = require('./4-rectangle');

const r1 = new Rectangle(2, 3);
console.log('Normal:');
r1.print();

console.log('Double:');
r1.double();
r1.print();

console.log('Rotate:');
r1.rotate();
r1.print();
5. Square #0
File: 5-square.js
Description: Write a class Square that defines a square and inherits from Rectangle of 4-rectangle.js. You must use the class notation for defining your class and extend. The constructor must take 1 argument size. The constructor of Rectangle must be called (by using super()).
javascript
Copy code
const Square = require('./5-square');

const s1 = new Square(4);
s1.print();
s1.double();
s1.print();
6. Square #1
File: 6-square.js
Description: Write a class Square that defines a square and inherits from Square of 5-square.js. You must use the class notation for defining your class and extends. Create an instance method called charPrint(c) that prints the rectangle using the character c. If c is undefined, use the character X.
javascript
Copy code
const Square = require('./6-square');

const s1 = new Square(4);
s1.charPrint();

s1.charPrint('C');
## 7. Occurrences

- File: 7-occurrences.js
- Description: Write a function that returns the number of occurrences in a list.

```javascript
const nbOccurences = require('./7-occurrences').nbOccurences;

console.log(nbOccurences([1, 2, 3, 4, 5, 6], 3));
console.log(nbOccurences([3, 2, 3, 4, 5, 3, 3], 3));
console.log(nbOccurences(["S", 12, "c", "S", "School", 8], "S"));
8. Esrever
File: 8-esrever.js
Description: Write a function that returns the reversed version of a list.
javascript
Copy code
const esrever = require('./8-esrever').esrever;

console.log(esrever([1, 2, 3, 4, 5]));
console.log(esrever(["School", 89, { id: 12 }, "String"]));
9. Log me
File: 9-logme.js
Description: Write a function that prints the number of arguments already printed and the new argument value.
javascript
Copy code
const logMe = require('./9-logme').logMe;

logMe("Hello");
logMe("Best");
logMe("School");
10. Number conversion
File: 10-converter.js
Description: Write a function that converts a number from base 10 to another base passed as an argument.
javascript
Copy code
const converter = require('./10-converter').converter;

let myConverter = converter(10);

console.log(myConverter(2));
console.log(myConverter(12));
console.log(myConverter(89));

<F12><F12><F12>## 11. Factor index

- File: 11-factor_index.js
- Description: Write a script that imports an array and computes a new array using the map function.

```javascript
const list = require('./100-data').list;

const factorIndex = list.map((value, index) => value * index);

console.log(list);
console.log(factorIndex);
12. Sorted occurrences
File: 12-sorted_occurrences.js
Description: Write a script that imports a dictionary of occurrences by user id and computes a dictionary of user ids by occurrence.
javascript
Copy code
const dict = require('./101-data').dict;

const sortedOccurrences = {};
Object.keys(dict).forEach((key) => {
  const occurrence = dict[key];
  if (!sortedOccurrences[occurrence]) {
    sortedOccurrences[occurrence] = [];
  }
  sortedOccurrences[occurrence].push(key);
});

console.log(sortedOccurrences);
13. Concat files
File: 13-concat_files.js
Description: Write a script that concatenates two files.
javascript
Copy code
const fs = require('fs');

const [, , fileA, fileB, fileC] = process.argv;

const contentA = fs.readFileSync(fileA, 'utf-8');
const contentB = fs.readFileSync(fileB, 'utf-8');
const concatenatedContent = contentA + contentB;

fs.writeFileSync(fileC, concatenatedContent);
## 14. Const or not const

- File: 14-mutable.js
- Description: Write a function that modifies the value of a variable.

```javascript
// This script intentionally attempts to reassign a const variable
const myVar = 333;
myVar = 555; // This will throw an error
15. Call me Moby
File: 15-call_me_moby.js
Description: Write a function that executes a given function 'n' times.
javascript
Copy code
// This script defines a function that calls another function n times
exports.callMeMoby = function (n, func) {
  for (let i = 0; i < n; i++) {
    func();
  }
};
16. Add me maybe
File: 16-add_me_maybe.js
Description: Write a function that increments a variable and calls another function.
javascript
Copy code
// This script defines a function that increments a variable and calls another function
exports.addMeMaybe = function (number, theFunction) {
  number++;
  theFunction(number);
};
17. Increment object
File: 17-increment_obj.js
Description: Write a script that increments a value in an object.
javascript
Copy code
const myObject = {
  value: 12,
};

myObject.incr = function () {
  this.value++;
};

console.log(myObject.value);
myObject.incr();
console.log(myObject.value);
18. Factorial
File: 18-factorial.js
Description: Write a script that computes and prints a factorial.
javascript
Copy code
const num = parseInt(process.argv[2]);

function factorial(n) {
  if (n === 0 || isNaN(n)) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

console.log(factorial(num));
