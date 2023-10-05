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
  - [Immediately Invoked Function Expression](#immediately-invoked-function-expression)
  - [Constructor Function](#constructor-function)
  - [Arrow Function](#arrow-function)
 
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

- #### Function Expression
Function expression is another way to define a function in JavaScript. Here we define a function using a variable and store the return value in avariable. 

Example:
```js
const add = function(a,b) {
   console.log(a+b);
}

add(2,3);
```

- #### Anonymous Function
Anonymous function declaration does not allow the function name. In the general function declaration syntex, the function name is attached in the function keyword but an anonymous function is declared only using the functioin keyword and a parenthesis.

Example:
```js
function(a,b) {
   console.log(a+b);
}
```

- #### Immediately Invoked Function Expression
The functions that are executed as soon as they are mounted are called `Immediately Invoked Function Expression(IIFE)`. It use the anonymous property of the function expression to execute its code. This is executed by wrapping the anonymous function in parentheses and ending it with the semicolon.

Example:
```js
(function () {
  console.log("Welcome to Javascript");
})();
```
 

  





















