# ES6 Basics

This project serves as a beginner's guide to the fundamentals of ECMAScript 2015 (ES6), also known as ES2015, which is a significant update to the JavaScript language. ES6 introduces many new features and syntax enhancements that make JavaScript more powerful and expressive. Whether you're new to JavaScript or looking to brush up on the latest language features, this project will provide you with a solid foundation.

## Table of Contents

1. [Introduction](#introduction)
2. [Key Features of ES6](#key-features-of-es6)
3. [Getting Started](#getting-started)
4. [Topics Covered](#topics-covered)
5. [Examples](#examples)
6. [Contributing](#contributing)
7. [License](#license)

## Introduction

ECMAScript 6, often referred to as ES6 or ES2015, is a major update to the JavaScript language. It brings several new features, syntax improvements, and enhanced functionality to make JavaScript development more efficient and readable. Understanding ES6 is essential for modern web development, as many frameworks and libraries now leverage these features.

## Key Features of ES6

Some of the key features introduced in ES6 include:

- **let and const**: Block-scoped variable declarations that replace `var`.
- **Arrow Functions**: A concise syntax for writing functions.
- **Template Literals**: A way to create multi-line strings and embed expressions.
- **Destructuring**: A method for extracting values from objects and arrays more easily.
- **Default Parameters**: Allows specifying default values for function parameters.
- **Classes**: A more structured way to create and work with objects.
- **Modules**: A standard system for organizing and reusing code.
- **Promises**: A better way to handle asynchronous operations.
- **Spread and Rest Operators**: Simplifies working with arrays and function arguments.
- **Map and Set**: New data structures for more advanced use cases.

## Getting Started

To start exploring ES6 basics:

1. Clone or download this repository to your local machine.
2. Open the project directory in your code editor of choice.
3. Explore the code examples and explanations provided in the project files.
4. Experiment with the examples by running them in your browser's developer console or a JavaScript environment.

## Topics Covered

This project covers a range of ES6 topics, including but not limited to:

- Variables and Scope
- Arrow Functions
- Template Literals
- Destructuring
- Default Parameters
- Classes
- Modules
- Promises
- Spread and Rest Operators
- Map and Set

## Examples

In this subheading, you'll find several code snippets and small projects illustrating various ES6 concepts. These examples are designed to help you understand how to use ES6 features in real-world scenarios.

### 1. Variables and Scope

```javascript
// ES6 introduced 'let' and 'const' for variable declarations.
let name = "John";
const age = 30;

name = "Jane"; // We can change 'let' variables.
// age = 31; // This will result in an error because 'const' variables cannot be reassigned.

// 'let' and 'const' are block-scoped.
if (true) {
  let blockScopedVar = "I'm in a block!";
}
// console.log(blockScopedVar); // This will result in an error because 'blockScopedVar' is not defined outside the block.

// 'var' is function-scoped and should be avoided in ES6.
```

### 2. Arrow Functions

```javascript
// Arrow functions provide a concise syntax for defining functions.
const add = (a, b) => a + b;

// Arrow functions with a single parameter can omit parentheses.
const square = num => num * num;

// Arrow functions can be used as anonymous functions.
setTimeout(() => {
  console.log("This function is executed after a delay.");
}, 1000);
```

### 3. Template Literals

```javascript
// Template literals allow you to create multi-line strings and embed expressions.
const name = "Alice";
const greeting = `Hello, ${name}!
Welcome to ES6 Basics.`;

console.log(greeting);
```

### 4. Destructuring

```javascript
// Destructuring allows you to extract values from objects and arrays.
const person = { firstName: "John", lastName: "Doe" };
const { firstName, lastName } = person;

console.log(firstName); // Output: John
console.log(lastName);  // Output: Doe

const numbers = [1, 2, 3, 4, 5];
const [first, second, ...rest] = numbers;

console.log(first); // Output: 1
console.log(second); // Output: 2
console.log(rest); // Output: [3, 4, 5]
```

### 5. Default Parameters

```javascript
// Default parameters allow you to set default values for function parameters.
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet(); // Output: Hello, Guest!
greet("Alice"); // Output: Hello, Alice!
```

### 6. Classes

```javascript
// ES6 introduces class syntax for defining object constructors.
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
}

const john = new Person("John", 30);
john.greet(); // Output: Hello, my name is John and I am 30 years old.
```

### 7. Modules

```javascript
// ES6 modules allow you to organize code into separate files.
// In 'math.js' file:
export function add(a, b) {
  return a + b;
}

// In 'main.js' file:
import { add } from './math.js';

const result = add(5, 3);
console.log(result); // Output: 8
```

### 8. Promises

```javascript
// Promises provide a way to handle asynchronous operations more cleanly.
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const data = { name: "Alice", age: 25 };
      // Simulate a successful API call
      resolve(data);
      // Simulate an error
      // reject("Failed to fetch data");
    }, 1000);
  });
}

fetchData()
  .then(data => {
    console.log("Data fetched successfully:", data);
  })
  .catch(error => {
    console.error("Error fetching data:", error);
  });
```

### 9. Spread and Rest Operators

```javascript
// Spread operator (...) is used to expand elements from an array or properties from an object.
const numbers = [1, 2, 3];
const newNumbers = [...numbers, 4, 5];

console.log(newNumbers); // Output: [1, 2, 3, 4, 5]

// Rest operator (...) collects remaining arguments into an array.
function sum(...args) {
  return args.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4)); // Output: 10
```

### 10. Map and Set

```javascript
// Map and Set are new data structures in ES6.
// Map allows you to store key-value pairs.
const personMap = new Map();
personMap.set("name", "Bob");
personMap.set("age", 28);

console.log(personMap.get("name")); // Output: Bob

// Set stores unique values.
const uniqueNumbers = new Set([1, 2, 2, 3, 3, 4]);

console.log(uniqueNumbers); // Output: Set { 1, 2, 3, 4 }
```

### 11. Object Shorthand and Computed Property Names

```javascript
// ES6 allows for shorter syntax when defining object properties.
const firstName = "Alice";
const lastName = "Johnson";

// Object shorthand
const person = { firstName, lastName };
console.log(person); // Output: { firstName: 'Alice', lastName: 'Johnson' }

// Computed property names
const dynamicKey = "age";
const personInfo = {
  name: "Bob",
  [dynamicKey]: 30,
};
console.log(personInfo.age); // Output: 30
```

### 12. Array Methods (forEach, map, filter)

```javascript
// ES6 provides handy array methods for iteration and manipulation.
const numbers = [1, 2, 3, 4, 5];

// forEach: Iterates through array elements.
numbers.forEach(num => console.log(num)); // Outputs each number.

// map: Creates a new array by applying a function to each element.
const doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8, 10]

// filter: Creates a new array with elements that pass a condition.
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```

### 13. Promises - Chaining

```javascript
// Promises can be chained for sequential asynchronous operations.
function fetchUserData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const user = { id: 1, username: "alice" };
      resolve(user);
    }, 1000);
  });
}

function fetchPosts(userId) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      const posts = ["Post 1", "Post 2", "Post 3"];
      resolve(posts);
    }, 800);
  });
}

fetchUserData()
  .then(user => {
    console.log("User data:", user);
    return fetchPosts(user.id);
  })
  .then(posts => {
    console.log("User posts:", posts);
  })
  .catch(error => {
    console.error("Error:", error);
  });
```

### 14. Async/Await

```javascript
// Async/await simplifies asynchronous code, making it look synchronous.
async function fetchData() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
    const data = await response.json();
    console.log("Data:", data);
  } catch (error) {
    console.error("Error:", error);
  }
}

fetchData();
```

### 15. SetTimeout with Promises

```javascript
// You can wrap setTimeout in a promise for asynchronous timing.
function delay(milliseconds) {
  return new Promise(resolve => {
    setTimeout(resolve, milliseconds);
  });
}

delay(2000)
  .then(() => {
    console.log("Two seconds have passed.");
  });
```

### 16. Generators

```javascript
// Generators allow you to pause and resume function execution.
function* countUp() {
  let count = 0;
  while (true) {
    yield count++;
  }
}

const counter = countUp();
console.log(counter.next().value); // Output: 0
console.log(counter.next().value); // Output: 1
```

### 17. Enhanced Object Literals

```javascript
// ES6 enhanced object literals provide concise syntax for object creation.
const name = "Alice";
const age = 30;

const person = {
  name,    // Shorthand for name: name
  age,     // Shorthand for age: age
  greet() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
};

person.greet();
```

### 18. Default Exports and Named Exports (Modules)

```javascript
// Modules can have default exports and named exports.
// math.js
export default function add(a, b) {
  return a + b;
}

// utils.js
export function multiply(a, b) {
  return a * b;
}

// main.js
import addFunction from './math.js';
import { multiply } from './utils.js';

console.log(addFunction(2, 3)); // Output: 5
console.log(multiply(2, 3));   // Output: 6
```

### 19. String Methods (startsWith, endsWith, includes)

```javascript
// ES6 adds useful string methods for checking and searching.
const text = "Hello, world!";

console.log(text.startsWith("Hello"));    // Output: true
console.log(text.endsWith("world!"));     // Output: true
console.log(text.includes("lo,"));         // Output: true
```

### 20. Object.assign

```javascript
// Object.assign allows you to copy properties from one object to another.
const person = { name: "Alice" };
const details = { age: 25, country: "USA" };

const merged = Object.assign({}, person, details);
console.log(merged); // Output: { name: 'Alice', age: 25, country: 'USA' }
```


## Contributing

If you'd like to contribute to this project by adding more examples or improving existing ones, please feel free to submit pull requests. Contributions from the community are highly encouraged!

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---