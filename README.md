# Content

- [Number](#number)
  - [Math 1](#math-1)
  - [Math 2](#math-2)
  - [Math 3](#math-3)
- [String Methods](#string-methods)
  - [Includes](#includes)
  - [StartsWith](#startswith)
  - [EndsWith](#endswith)
  - [IndexOf](#indexof)
  - [Slice](#slice)
  - [ToLowerCase](#tolowercase)
  - [ToUpperCase](#touppercase)
  - [Replace](#replace)
  - [ReplaceAll](#replaceall)
- [Prototype](#prototype)
- [Window](#window)
  - [Console](#console)
  - [Document](#document)
  - [Location](#location)
  - [Alert](#alert)
  - [Open](#open)
- [Function](#function)
  - [Function Expression](#function-expression)
  - [Anonymous Function](#anonymous-function)
  - [Immediately Invoked Function Expression(IIFE)](#immediately-invoked-function-expressioniife)
  - [Constructor Function](#constructor-function)
  - [Arrow Function](#arrow-function)
- [Array](#array)
	- [Array Methods](#array-methods)
	  	- [Array.at](#arrayat)
	  	- [Array.concat](#arrayconcat)
	  	- [Array.every](#arrayevery)
	  	- [Arry.filter](#arrayfilter)
	  	- [Array.find](#arrayfind)
	  	- [Aray.findIndex](#arrayfindindex)
	  	- [Array.forEach](#arrayforeach)
	  	- [Array.includes](#arrayincludes)
   		- [Array.indexOf](#arrayindexof)
     	- [Array.map](#arraymap)
      	- [Array.push](#arraymap)
      	- [Array.pop](#arraypop)
- [For loop](#for-loop)      
   	 
     
 
 
### Number

- #### Math 1
```js
let finalResult;

let evenOddResult;

// Add your code here

const num1 = 2;
const num2 = 6;
const num3 = 8;
const num4 = 14;

const sum = num1 + num2;
const substract = num4 - num3;

finalResult = sum * substract;
evenOddResult = finalResult % 2;
```

- #### Math 2
```js
// Final result should be 4633.33
// Add/update your code here

let result = 7 + 13 / 9 + 7;
let result2 = 100 / 2 * 6;

result = result * result2;
result = result.toFixed(2);

const type = typeof result;

let finalResult = result;

if(type === 'string') {
  finalNumber = Number(finalResult);
}
```

- #### Math 3
```js
// Statement 1: The elephant weighs less than the mouse
const eleWeight = 1000;
const mouseWeight = 2;

// Statement 2: The Ostrich is taller than the duck
const ostrichHeight = 2;
const duckHeight = 0.3;

// Statement 3: The two passwords match
const pwd1 = 'stromboli';
const pwd2 = 'stROmBoLi';

// Add your code here
const weightComparison = eleWeight < mouseWeight;
const heightComparison = ostrichHeight > duckHeight;
const pwdMatch = pwd1 === pwd2
```

### String Methods

- #### Includes
If we want to find a substring in a string,we can use `includes` method. 

 ```js
const browserType = "mozilla";
const searchedString = "zilla"

if (browserType.includes(searchedString)) {
  console.log("Found " + searchedString);
} else {
  console.log(`No ${searchedstring} here!`);
}
```

- #### StartsWith
If we want to know a string starts with a substring,we can use `startswith`method.

```js
const browserType = "mozilla";

if (browserType.startsWith("zilla")) {
  console.log("Found zilla!");
} else {
  console.log("No zilla here!");
}
```

- #### EndsWith
Using `endswith`method we can know that a string ends with a substring.

```js
const browserType = "mozilla";

if (browserType.endsWith("zilla")) {
  console.log("Found zilla!");
} else {
  console.log("No zilla here!");
}
```

- #### IndexOf
`indexOf`method define the position of the substring in a string.
```js
const tagline = "MDN - Resources for developers, by developers";
console.log(tagline.indexOf("e")); //Output will be 7
```

If there is no existance in a substring then it will return `-1`.
```js
const tagline = "MDN - Resources for developers, by developers";
console.log(tagline.indexOf("x")); //Output will be -1
```

To find the second occurrence, we can pass a second parameter to this method that is greater than the index of the previous occurrence.
```js
const firstOccurrence = tagline.indexOf("developers");
const secondOccurrence = tagline.indexOf("developers", firstOccurrence + 1);

console.log(firstOccurrence); // Output will be 20
console.log(secondOccurrence); // Output will be 35
```

- #### Slice
You can extract a substring from a string using the `slice` method. It contain two parameter, start & end parameter.Start parameter is inclusive & end parameter is exclusive.
```js
const browserType = "mozilla";
console.log(browserType.slice(1, 4)); // Output will be "ozi"
 ```
```js
If we want to remaining character from the certain character,we do  not have second parameter.We only need to inclued character position from where we want to extract.
browserType.slice(2); // "zilla"
```

- #### toLowerCase
In a string we can convert all charecter to lower if we can use `toLowerCase` string method.
```js
const radData = "My NaMe Is MuD";
console.log(radData.toLowerCase());
```

- #### toUpperCase
In a string we can convert all charecter to uppper if we can use `toUpperCase` string method.
```js
const radData = "My NaMe Is MuD";
console.log(radData.toUpperCase());
```

- #### Replace
To use `replace` string method , we can update string to replace substring in a string. There are two parameters- the string we want to replace and the string we want to replace it with. It will not change the original string rather than it will create a new string.

```js
const browserType = "mozilla";
const updated = browserType.replace("moz", "van");

console.log(updated); // "vanilla"
console.log(browserType); // "mozilla"
```

- #### ReplaceAll
`replaceAll` string method change all occurrence. It takes two parameter: first parameter that will be replaced and second parameter that will replace the string of first parameter. So the main difference `replace` & `replaceAll` is `replace` only replaces first occurrence and `replaceAll` replaces all occurrence of the string.

```js
let quote = "To be or not to be";
quote = quote.replaceAll("be", "code");

console.log(quote); // "To code or not to code"
```

### Prototype

```js
const electronicsDevice = {
  id: "",
  name: "",
  type: "",
  weight:"",
  color: "",

  __proto__: {
    isVerified: false,
        
    addDeviceToStore(id, name, type, weight, color) {
      this.id = id;
      this.name = name;
      this.type = type;
      this.weight = weight;
      this.color = color;

      console.log('Device is added to the store.');
    },

    verifyDevice(id, type) {
      if(id !== this.id || type !== this.type) return;

      this.isVerified = true;
    }
  }
}

electronicsDevice.addDeviceToStore('1', 'iPhone 15', 'phone', '190gm', 'purple');
electronicsDevice.verifyDevice('2', 'phone');

if(electronicsDevice.isVerified) {
  console.log('Your device is purchased from our store.');
} else {
  console.log('The device is not purchased from our store.');
}

electronicsDevice.addDeviceToStore('2', 'Macbook Pro', 'laptop', '1kg', 'silver');
electronicsDevice.verifyDevice('2', 'laptop');

if(electronicsDevice.isVerified) {
  console.log('Your device is purchased from our store.');
} else {
  console.log('The device is not purchased from our store.');
}
```

### Window
Every browser gives an object. It is called `window`. A browser window is represented by the `window` object. Through `window` object, we can access the browser’s methods and attributes as the global object in the browser environment. So this is not javascript thing. It is all about browser. But all global javascript objects, functions and variables automatically become members of the window object. To access those variables, functions or objects, you can call those with or without `window`. For example: 

```js
// The output of the below code is same. Cause you can call it with 'window.location' or only 'location'
console.log(window.location); // It's also pointing to the location object of the window
console.log(location); // It's also pointing to the location object of the window

a = 5; // As this is global object, it will add to the window object automatically as a property.

console.log(a); // output will be 5
console.log(window.a); // output will be 5
```

There are lots of methods and attributes in the `window` object. Here are the list of some most useful methods and property used in development.

- #### Console
To log information we can use this methods of `window` object.
```js
console.log("Loggin information");
console.error("Loggin error");
console.info("Logging as info");
```

- #### Document
To access HTML, it is used widely. For example:
```js
document.getElementById('root') // Returns the element that has the ID "root"
```

- #### Location
The `location` refers the `Location` object, which has data about the current URL of that page. Such as:
```js
location.hostname; // Output will be 'github.com'
location.pathname; // Output will be '/mahmuda-alam/homework'
```

- #### LocalStorage
This is a useful methods of `window` Object. It is used to save data in the browser. But the storage capacity of the browser is low. Usecase:
```js
localStorage.setItem('key', 'value'); // Save this key-value pair in the browser which is located to the 'Application' tab of the browser
localStorage.getItem('key'); // To Retrieve value from browser localStorage, it is used
localStorage.removeItem('key'); // To remove an item from localStorage
```

- #### Alert
To show alert, we can use this method. For example:
```js
alert('This is an alert message');
```

- #### Open
This will open new window in the browser.
```js
open('https://github.com/mahmuda-alam/homework'); 
```

### Function
Functions are one of the fundamental building block in javascript. A function is a set of statements that take input, do some specific computation and produce output. The idea is to put some commonly and repeatedly done tasks together make a function so that instead of writing the same code again and again for different inputs, we can call that function.

A basic javascript function:
```js
function myFunction(n1, n2) {
  return n1 / n2;
}

const value = myFunction(8, 2);
console.log(value);
```

There are different ways to decalre a function. Here are some examples: 

- #### Function Expression
Function expression is another way to define a function in JavaScript. Here we define a function using a variable and store the return value in a variable. 

Example:
```js
const add = function(a, b) {
   console.log(a + b);
}

add(2, 3);
```

- #### Anonymous Function
Anonymous function declaration does not allow the function name. In the general function declaration syntax, the function name is attached in the function keyword but an anonymous function is declared only using the function keyword and a parenthesis.

Example:
```js
function(a, b) {
   console.log(a + b);
}
```

- #### Immediately Invoked Function Expression(IIFE)
The functions that are executed as soon as they are mounted are called `Immediately Invoked Function Expression(IIFE)`. It use the anonymous property of the function expression to execute its code. This is executed by wrapping the anonymous function in parentheses and ending it with the semicolon.

Example:
```js
(function () {
  console.log("Welcome to Javascript");
})();
```

- #### Constructor Function
Constructor function create a function object which executes in the global scope. It can be used to create multiple object that are similar. The constructor function has similar functionalities as the function expression. It is called with the `new` keyword to create an object. Constructor function aslo can be used with the `this` keyword.

Example:
```js
function Person() {
   this.name = "John",
   this.age = 20,
}

const person = new Person();

console.log(person.name);
console.log(person.age);
```

- #### Arrow Function
Arrow function is used to shorten the code. Here we do not use `function` keyword and use the arrow symbol. It is generally a cleaner way of creating JavaScript functions and it is similar to the function expression.

```js
 add = (a, b) => a + b; 
	
console.log(add(3, 2)); 
```


# Array
JavaScript Array is a single variable that is used to store elements of different data types. JavaScript arrays are zero-indexed.Arrays are used when we have a list of items. An array allows you to store several values with the same name and access them by using their index number.

Example:
 ```js
const cars = ["Saab", "Volvo", "BMW"];

const cars = [];
cars[0]= "Saab";
cars[1]= "Volvo";
cars[2]= "BMW";
```

- ### Array Methods
There are described some methods of `Array`: 

- #### Array.at
The `at` methods of array takes an integer value and returns the item of the index. It allows positive and negetive integer. Negative integers count back from the last item in the array.

Example:
```js
const arr = [5, 12, 8, 130, 44];
let index = 3;
let value = arr.at(index);

console.log(`The value of index ${index} is: ${value}`); // Output will be 130

index = -3;
value = arr.at(index)

console.log(`The value of index ${index} is: ${value}`); // Output will be 8
```

- #### Array.concat
The `concat` method of array is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

	Example:
```js
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);

console.log(array3);
// Output will be: Array ["a", "b", "c", "d", "e", "f"]
```

- #### Array.every
The `every` method of array tests every element that pass the test implemented by the provided function. It returns a `Boolean` value.

Example:
```js
let greaterFive = (currentValue) => currentValue > 5 ;

const array = [1, 2, 3, 4, 5, 6, 7];

console.log(array.every(greaterFive)); // Output will be false

lessnine = (currentValue) => currentValue < 9 ;

console.log = (array.every(lessnine)); // Output will be true
```

- #### Array.filter
The `Filter` method of array creates a shallow copy of a portion of a given array, filtered down to just the elements from the given array that pass the test implemented by the provided function.

	Example:
```js
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter((word) => word.length > 6);

console.log(result);
// Output will be : Array ["exuberant", "destruction", "present"]
```

- #### Array.find
The `Find` method of array  returns the value of the first element in an array that pass the test in a testing function.

  Example:
  ```js
  const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  const found = arr.find(element => element > 5);

  console.log(found); // Output will be 6
  ```

- #### Array.findIndex
The `findIndex` method of array is used to return the first index of the element in a given array that satisfies the provided testing function. Otherwise, if no data is found then the value of -1 is returned.

Example:
```js
const array1 = [5, 12, 8, 130, 44];

const isLargeNumber = (element) => element > 13;

console.log(array1.findIndex(isLargeNumber)); // output will be 3
```

- #### Array.forEach
The `forEach` method of array executes a provided function once for each array element.

Example:
```js
const arr = [1, 2, 3]
arr.forEach(element => {
console.log(element);
});
// Output will be : 1
// Output will be : 2
// Output will be : 3
```

- #### Array.includes
The `includes` method of array checks if an array includes the element that passes the condition, returning true or false as appropriate.

Example:
```js
const array1 = [1, 2, 3];

console.log(array1.includes(2));
// Output will be : true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// Output will be: true

console.log(pets.includes('at'));
// Output will be : false
```

- #### Array.indexOf
The `indexOf` method of array returns the index of the first occurrence of the specified element in the array, or -1 if it is not found.

Example:
```js
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];

console.log(beasts.indexOf('bison'));
// Output will be : 1

// Start from index 2
console.log(beasts.indexOf('bison', 2));
// Output will be : 4

console.log(beasts.indexOf('giraffe'));
// Output will be : -1
```

- #### Array.map
The `map` method of array creates a new array populated with the results of calling a provided function on every element in the calling array.

Example:
```js
const arr [1, 2, 3, 4, 5, 6]
const mapped = arr.map(element => element + 30);

console.log(mapped); // Output will be : [31, 32, 33, 34, 35, 36]
```

- #### Array.push
The `push` method of array adds the specified elements to the end of an array and returns the new length of the array.

Example:
```js
const animals = ['pigs', 'goats', 'sheep'];

const count = animals.push('cows');
console.log(count); // Output will be : 4

console.log(animals); // Output: Array ["pigs", "goats", "sheep", "cows"]

animals.push('chickens', 'cats', 'dogs');
console.log(animals); // Output will be : Array ["pigs", "goats", "sheep", "cows", "chickens", "cats", "dogs"]
```

- #### Array.pop
The `pop` method of Array removes the last element from an array and returns that element. This method changes the length of the array.

Example:
```js
const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];

console.log(plants.pop()); // Output will be : "tomato"

console.log(plants); // Output will be : Array ["broccoli", "cauliflower", "cabbage", "kale"]

plants.pop();

console.log(plants); // Output will be : Array ["broccoli", "cauliflower", "cabbage"]
```

# For loop
Looping in programming languages is a feature that facilitates the execution of a set of instructions repeatedly until some condition evaluates and becomes false. Again, there are many types of loops, but here we will only look at the for loop. 
We come across for loop which provides a brief and systematic way of writing the loop structure. Syntax:

```js
for(statement1; statement2; statement3) {
code here....
}
```
1. Statement1: it is the initialization of the counter. It is executed once before the execution of the code block.
2. Statement2: It is the testing statement that defines the condition for executing the code block It must return a boolean value. It is also an entry-controlled loop as the condition is checked before the execution of the loop statements.
3. Statement3: It is the increment or decrement of the counter & executed (every time) after the code block has been executed.
   
Example:
```js
function isLeapear(year) {
    if(year % 4 ===0 && year % 100 !== 0 || year % 400 === 0) {
        return true
    } else {
        return false
    }
}

const years = [1988, 1990, 1994, 1997, 2000, 2005, 2012, 2015, 2020,2023,]

for(let i = 0; i < years.length; i++) {
    let x = isLeapear(years[i])

    if(x === true) {
        console.log(years[i] + ' is a leapyear');
    } else {
        console.log(years[i] + ' is not a leapyear');
    }
}
```
  





















