# 📘 JavaScript Built-in Functions — GitHub README

Welcome to the ultimate guide for JavaScript's built-in functions! 🚀
This README will walk you through the most commonly used functions, complete with examples, so you can level up your JS skills.

---

## 🖥️ **Console & Alerts**

### 🔸 `console.log()` → Logs output to the console.
```javascript
console.log("Hello, World!"); // Output: Hello, World!
```

### 🔸 `console.error()` → Logs an error message to the console.
```javascript
console.error("This is an error!");
```

### 🔸 `console.warn()` → Logs a warning message.
```javascript
console.warn("This is a warning!");
```

### 🔸 `console.info()` → Logs an informational message.
```javascript
console.info("This is an info message.");
```

### 🔸 `console.table()` → Displays tabular data as a table.
```javascript
let users = [
  { name: "Alice", age: 25 },
  { name: "Bob", age: 30 }
];
console.table(users);
```

### 🔸 `console.group()` / `console.groupEnd()` → Creates a collapsible console group.
```javascript
console.group("My Group");
console.log("Inside the group");
console.groupEnd();
```

### 🔸 `console.count()` → Logs the number of times it’s called.
```javascript
console.count("Counter");
console.count("Counter");
```

### 🔸 `console.time()` / `console.timeEnd()` → Measures time between calls.
```javascript
console.time("Timer");
// Some operation
console.timeEnd("Timer");
```

### 🔸 `alert()` → Shows a popup alert.
```javascript
alert("This is an alert box!");
```

### 🔸 `prompt()` → Asks for user input.
```javascript
let name = prompt("What is your name?");
console.log("Hello, " + name);
```

### 🔸 `confirm()` → Asks for confirmation (OK/Cancel).
```javascript
let isConfirmed = confirm("Are you sure?");
console.log(isConfirmed); // true or false
```
---

## 🧠 **String Functions**

### 🔸 `charAt()` → Returns the character at a specified index.

```javascript
let str = "JavaScript";
console.log(str.charAt(3)); // Output: a
```

### 🔸 `charCodeAt()` → Returns the Unicode of the character at a given index.

```javascript
console.log(str.charCodeAt(0)); // Output: 74 (Unicode for 'J')
```

### 🔸 `at()` → Returns the character at a given index (supports negative indexing).

```javascript
console.log(str.at(-1)); // Output: t
```

### 🔸 `concat()` → Joins two or more strings.

```javascript
let greeting = "Hello";
let name = "World";
console.log(greeting.concat(" ", name)); // Hello World
```

### 🔸 `includes()` → Checks if a string contains a substring.

```javascript
console.log(str.includes("Script")); // true
```

### 🔸 `indexOf()` / `lastIndexOf()` → Finds the index of a substring.

```javascript
console.log(str.indexOf("a")); // 1
console.log(str.lastIndexOf("a")); // 3
```

### 🔸 `startsWith()` / `endsWith()` → Checks the start or end of a string.

```javascript
console.log(str.startsWith("Java")); // true
console.log(str.endsWith("Script")); // true
```

### 🔸 `slice()` → Extracts part of a string.

```javascript
console.log(str.slice(0, 4)); // Java
```

### 🔸 `substring()` → Returns part of a string between two indices.

```javascript
console.log(str.substring(4, 10)); // Script
```

### 🔸 `substr()` → Returns a substring (deprecated, but still supported).

```javascript
console.log(str.substr(4, 6)); // Script
```

### 🔸 `toUpperCase()` / `toLowerCase()` → Changes string case.

```javascript
console.log(str.toUpperCase()); // JAVASCRIPT
console.log(str.toLowerCase()); // javascript
```

### 🔸 `trim()` / `trimStart()` / `trimEnd()` → Removes whitespace.

```javascript
let messyStr = "   Hello World!   ";
console.log(messyStr.trim()); // Hello World!
console.log(messyStr.trimStart()); // "Hello World!   "
console.log(messyStr.trimEnd()); // "   Hello World!"
```

### 🔸 `padStart()` / `padEnd()` → Pads a string with characters.

```javascript
console.log(str.padStart(15, "*")); // ***JavaScript
console.log(str.padEnd(15, "*")); // JavaScript***
```

### 🔸 `repeat()` → Repeats a string.

```javascript
console.log(str.repeat(3)); // JavaScriptJavaScriptJavaScript
```

### 🔸 `replace()` / `replaceAll()` → Replaces parts of a string.

```javascript
console.log(str.replace("Java", "Type")); // TypeScript
console.log(str.replaceAll("a", "@")); // J@v@Script
```

### 🔸 `split()` → Splits a string into an array.

```javascript
console.log(str.split("a")); // [ 'J', 'v', 'Script' ]
```

### 🔸 `match()` / `matchAll()` → Matches a string with a regular expression.

```javascript
let sentence = "The rain in Spain stays mainly in the plain.";
console.log(sentence.match(/ain/g)); // [ 'ain', 'ain', 'ain', 'ain' ]

let matches = sentence.matchAll(/ain/g);
console.log([...matches]);
```

### 🔸 `localeCompare()` → Compares two strings in the current locale.

```javascript
console.log("apple".localeCompare("banana")); // -1
```

### 🔸 `normalize()` → Normalizes a string to Unicode form.

```javascript
let accented = "é";
console.log(accented.normalize("NFD")); // é (split into e + ´)
```
---


## 🟠 **Object Functions**

### 🔸 `Object.keys()` → Returns an array of an object’s keys.

```javascript
const user = { name: "Alice", age: 25, country: "USA" };
console.log(Object.keys(user)); // [ 'name', 'age', 'country' ]
```

### 🔸 `Object.values()` → Returns an array of an object’s values.

```javascript
console.log(Object.values(user)); // [ 'Alice', 25, 'USA' ]
```

### 🔸 `Object.entries()` → Returns an array of key-value pairs.

```javascript
console.log(Object.entries(user)); // [ ['name', 'Alice'], ['age', 25], ['country', 'USA'] ]
```

### 🔸 `Object.assign()` → Copies properties from one object to another.

```javascript
const target = { a: 1 };
const source = { b: 2, c: 3 };
Object.assign(target, source);
console.log(target); // { a: 1, b: 2, c: 3 }
```

### 🔸 `Object.freeze()` → Prevents modification of object properties.

```javascript
const obj = { key: "value" };
Object.freeze(obj);
obj.key = "newValue";
console.log(obj.key); // value (unchanged)
```

### 🔸 `Object.seal()` → Prevents adding or deleting properties but allows modification.

```javascript
Object.seal(user);
user.name = "Bob";
delete user.age;
console.log(user); // { name: 'Bob', age: 25, country: 'USA' }
```

### 🔸 `Object.create()` → Creates a new object with a specified prototype.

```javascript
const proto = { greet() { console.log("Hello!"); } };
const objWithProto = Object.create(proto);
objWithProto.greet(); // Hello!
```

### 🔸 `Object.hasOwnProperty()` → Checks if an object has a property (ignores prototype).

```javascript
console.log(user.hasOwnProperty("age")); // true
console.log(user.hasOwnProperty("toString")); // false (inherited)
```

### 🔸 `Object.getOwnPropertyNames()` → Returns all property names (even non-enumerable).

```javascript
console.log(Object.getOwnPropertyNames(user)); // [ 'name', 'age', 'country' ]
```

### 🔸 `Object.getPrototypeOf()` → Returns the prototype of an object.

```javascript
console.log(Object.getPrototypeOf(user)); // {} (or base Object prototype)
```

### 🔸 `Object.setPrototypeOf()` → Sets the prototype of an object.

```javascript
const newProto = { greet() { console.log("Hi!"); } };
Object.setPrototypeOf(user, newProto);
user.greet(); // Hi!
```

### 🔸 `Object.is()` → Compares two values (like `===` but handles NaN properly).

```javascript
console.log(Object.is(NaN, NaN)); // true
console.log(Object.is(0, -0)); // false
```

---


## 🔵 **Array Functions**

### 🔸 `Array.isArray()` → Checks if a value is an array.

```javascript
console.log(Array.isArray([1, 2, 3])); // true
console.log(Array.isArray("Hello")); // false
```

### 🔸 `push()` / `pop()` → Add/remove elements from the end of an array.

```javascript
const arr = [1, 2, 3];
arr.push(4);
console.log(arr); // [1, 2, 3, 4]
arr.pop();
console.log(arr); // [1, 2, 3]
```

### 🔸 `shift()` / `unshift()` → Remove/add elements at the start of an array.

```javascript
arr.shift();
console.log(arr); // [2, 3]
arr.unshift(0);
console.log(arr); // [0, 2, 3]
```

### 🔸 `concat()` → Combines arrays.

```javascript
const arr2 = [4, 5];
const combined = arr.concat(arr2);
console.log(combined); // [0, 2, 3, 4, 5]
```

### 🔸 `slice()` → Returns a portion of an array.

```javascript
console.log(arr.slice(1, 3)); // [2, 3]
```

### 🔸 `splice()` → Adds/removes elements in an array.

```javascript
arr.splice(1, 1, "new");
console.log(arr); // [0, 'new', 3]
```

### 🔸 `forEach()` → Iterates over each element.

```javascript
arr.forEach((item) => console.log(item));
```

### 🔸 `map()` → Transforms elements in an array.

```javascript
const squared = arr.map((num) => num * num);
console.log(squared); // [0, NaN, 9]
```

### 🔸 `filter()` → Filters elements based on a condition.

```javascript
const nums = [1, 2, 3, 4];
const even = nums.filter((num) => num % 2 === 0);
console.log(even); // [2, 4]
```

### 🔸 `reduce()` → Reduces an array to a single value.

```javascript
const sum = nums.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // 10
```

### 🔸 `find()` → Finds the first element that matches a condition.

```javascript
const found = nums.find((num) => num > 2);
console.log(found); // 3
```

### 🔸 `findIndex()` → Finds the index of the first matching element.

```javascript
console.log(nums.findIndex((num) => num > 2)); // 2
```

### 🔸 `indexOf()` / `lastIndexOf()` → Finds index of an element.

```javascript
console.log(nums.indexOf(3)); // 2
console.log(nums.lastIndexOf(3)); // 2
```

### 🔸 `includes()` → Checks if an array contains an element.

```javascript
console.log(nums.includes(2)); // true
```

### 🔸 `join()` → Joins elements into a string.

```javascript
console.log(nums.join(" - ")); // 1 - 2 - 3 - 4
```

### 🔸 `reverse()` → Reverses the array.

```javascript
console.log(nums.reverse()); // [4, 3, 2, 1]
```

### 🔸 `sort()` → Sorts elements.

```javascript
console.log(nums.sort()); // [1, 2, 3, 4]
```

### 🔸 `every()` → Tests if all elements match a condition.

```javascript
console.log(nums.every((num) => num > 0)); // true
```

### 🔸 `some()` → Tests if at least one element matches a condition.

```javascript
console.log(nums.some((num) => num > 3)); // true
```

### 🔸 `fill()` → Fills elements with a static value.

```javascript
console.log(nums.fill(0, 1, 3)); // [1, 0, 0, 4]
```

### 🔸 `copyWithin()` → Copies elements within an array.

```javascript
console.log(nums.copyWithin(1, 2)); // [1, 0, 4, 4]
```

---


## 🛠️ **Utility Functions**

### 🔸 `parseInt()` → Parses a string and returns an integer.

```javascript
console.log(parseInt("42")); // 42
console.log(parseInt("101", 2)); // 5 (binary to decimal)
```

### 🔸 `parseFloat()` → Parses a string and returns a floating-point number.

```javascript
console.log(parseFloat("3.14")); // 3.14
```

### 🔸 `isNaN()` → Checks if a value is NaN (Not a Number).

```javascript
console.log(isNaN("Hello")); // true
console.log(isNaN(123)); // false
```

### 🔸 `isFinite()` → Checks if a value is a finite number.

```javascript
console.log(isFinite(100)); // true
console.log(isFinite(Infinity)); // false
```

### 🔸 `encodeURI()` / `decodeURI()` → Encode and decode URIs.

```javascript
const uri = "https://example.com?name=John Doe";
const encoded = encodeURI(uri);
console.log(encoded);
console.log(decodeURI(encoded));
```

### 🔸 `encodeURIComponent()` / `decodeURIComponent()` → Encode and decode URI components.

```javascript
const query = "name=John Doe&age=25";
const encodedComponent = encodeURIComponent(query);
console.log(encodedComponent);
console.log(decodeURIComponent(encodedComponent));
```

### 🔸 `btoa()` / `atob()` → Encode and decode Base64 strings.

```javascript
const str = "Hello World";
const encodedStr = btoa(str);
console.log(encodedStr);
console.log(atob(encodedStr));
```

### 🔸 `typeof` → Returns the type of a value.

```javascript
console.log(typeof 42); // 'number'
console.log(typeof "Hello"); // 'string'
```

### 🔸 `instanceof` → Checks if an object is an instance of a constructor.

```javascript
console.log([] instanceof Array); // true
console.log({} instanceof Object); // true
```

### 🔸 `Object.keys()` → Returns an array of an object's keys.

```javascript
const obj = { a: 1, b: 2 };
console.log(Object.keys(obj)); // ['a', 'b']
```

### 🔸 `Object.values()` → Returns an array of an object's values.

```javascript
console.log(Object.values(obj)); // [1, 2]
```

### 🔸 `Object.entries()` → Returns an array of key-value pairs.

```javascript
console.log(Object.entries(obj)); // [['a', 1], ['b', 2]]
```

### 🔸 `Object.assign()` → Copies properties from one object to another.

```javascript
const target = { a: 1 };
const source = { b: 2 };
Object.assign(target, source);
console.log(target); // { a: 1, b: 2 }
```

### 🔸 `Object.freeze()` → Freezes an object to prevent modifications.

```javascript
const frozenObj = Object.freeze({ a: 1 });
frozenObj.a = 2; // Won't change
console.log(frozenObj); // { a: 1 }
```

### 🔸 `Object.seal()` → Seals an object, preventing new properties but allowing modifications.

```javascript
const sealedObj = Object.seal({ a: 1 });
sealedObj.a = 2; // Can modify existing properties
sealedObj.b = 3; // Won't add new property
console.log(sealedObj); // { a: 2 }
```

---


## 🕒 **Date Functions**

### 🔸 `Date()` → Creates a new date object.

```javascript
const date = new Date();
console.log(date); // Current date and time
```

### 🔸 `getFullYear()` → Gets the year.

```javascript
console.log(date.getFullYear());
```

### 🔸 `getMonth()` → Gets the month (0-11).

```javascript
console.log(date.getMonth()); // 0 for January
```

### 🔸 `getDate()` → Gets the day of the month.

```javascript
console.log(date.getDate());
```

### 🔸 `getDay()` → Gets the day of the week (0-6).

```javascript
console.log(date.getDay()); // 0 for Sunday
```

### 🔸 `getHours()` / `getMinutes()` / `getSeconds()` → Gets time components.

```javascript
console.log(date.getHours());
console.log(date.getMinutes());
console.log(date.getSeconds());
```

### 🔸 `getTime()` → Gets the timestamp (ms since 1970).

```javascript
console.log(date.getTime());
```

### 🔸 `setFullYear()` / `setMonth()` / `setDate()` → Sets date components.

```javascript
date.setFullYear(2025);
date.setMonth(11); // December
date.setDate(25);
console.log(date);
```

### 🔸 `toDateString()` → Converts to a readable date string.

```javascript
console.log(date.toDateString());
```

### 🔸 `toTimeString()` → Converts to a readable time string.

```javascript
console.log(date.toTimeString());
```

### 🔸 `toISOString()` → Converts to ISO 8601 format.

```javascript
console.log(date.toISOString());
```

### 🔸 `toLocaleDateString()` / `toLocaleTimeString()` → Converts to locale-specific date/time.

```javascript
console.log(date.toLocaleDateString());
console.log(date.toLocaleTimeString());
```

### 🔸 `Date.parse()` → Parses a date string.

```javascript
const timestamp = Date.parse("2025-12-25T10:00:00");
console.log(timestamp);
```

### 🔸 `Date.now()` → Gets the current timestamp.

```javascript
console.log(Date.now());
```

---











