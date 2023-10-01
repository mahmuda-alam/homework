# Content

- [Number](#number)
  - [Math 1](#math-1)
  - [Math 2](#math-2)
  - [Math 3](#math-3)
- [String Methods](#string-methods)
  - [Includes](#includes)
  - [Startswith](#startswith)
  - [Endswith](#endswith)
    
 
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

- #### Startswith
If we want to know a string starts with a substring,we can use `startswith`method.

```js
const browserType = "mozilla";

if (browserType.startsWith("zilla")) {
  console.log("Found zilla!");
} else {
  console.log("No zilla here!");
}
```

- #### Endswith
Using `endswith`method we can know that a string ends with a substring.

```js
const browserType = "mozilla";

if (browserType.endsWith("zilla")) {
  console.log("Found zilla!");
} else {
  console.log("No zilla here!");
}
```



























