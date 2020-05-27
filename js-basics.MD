*Types*

**Primitives**

<ul>
  <li>String</li>
  <li>Number</li>
  <li>Boolean</li>
  <li>null</li>
  <li>undefined</li>
  <li>Symbol</li>
</ul>

**Complex**

<ul>
  <li>Object</li>

```js
let student = {
  name: "Ritwick",
  rollno: 6,
  value: function(value) {
    return (value + 1);
  }
}

console.log(student.name); // "ritwick"
console.log(student.rollno); // 6
console.log(student.value(1)); // 2

//Object Destructuring
let { name, rollno } = student;
console.log(name);
```

<li>Array</li>


```js
let arr = new Array(1, 2); // [1, 2]
let arr = [1, 2]; // [1, 2]

// Push operation in arrays

arr.push(3);
console.log(arr); // [1, 2, 3]

// Pop operations in arrays

arr.pop();
console.log(arr); // [1, 2]
```

<li>Function</li>

```js
function func1(name) {
  return "Hello " + name + "!";
}

func1("Ritwick"); // "Hello Ritwick!"


//Arrow functions
let func1 = (name) => {
  console.log("Hello " + name + "!");
}

func1("Ritwick"); // "Hello Ritwick!"

// Another way
let func1 = (name) => {
  console.log(`Hello ${name}!`);
}

func1("Ritwick"); // "Hello Ritwick!"
```
</ul>

**let vs var vs const**

```js
// var
function varImplementation() {
  for (var i = 0; i < 5; i++) {
    console.log(i); //0 1 2 3 4
  }

  console.log(i); //5
}

//let

function varImplementation() {
  for (let i = 0; i < 5; i++) {
    console.log(i); //0 1 2 3 4
  }

  console.log(i); // undefined
}

// const
const temp = 10;
temp = temp + 10; // TypeError
```

**== vs ===**

```js
console.log(2 == "2"); // true
console.log(2 === "2"); // false (matches type too)
```

**typeof**

```js
typeof(2); // "number"
typeof("ritwick"); // "string"

let variable;
typeof(variable); // undefined

const arr = [1];
typeof(arr[1]); // undefined
```

**null vs undefined**

<ul>
  <li><strong>null:</strong> It is an assigned value.</li>
  <li><strong>undefined:</strong> It simply means a variable has been declared but not initialized.</li>
</ul>

**Array**

<ul>
<li>Push and Pop</li>

```js
//  Push
let arr = ["Ritwick"];
arr.push("Shashank"); //  [ "Ritwick", "Shashank" ]

//  Pop
arr.pop(); // [ "Ritwick" ]
```

<li>Shift and Unshift</li>

```js
//  Shift
let arr = ["Ritwick"];
const name = arr.shift(); //  Ritwick

//  Unshift
let arr = ["Ritwick", "Shashank"];
arr.unshift("Aakash"); // [ "Aakash", "Ritwick", "Shashank" ]
```

<li>Concat</li>

```js
let arr = ["Ritwick"];
let arr1 = ["Aakash"];
arr = arr.concat(arr1); // [ "Ritwick", "Aakash" ]
```

<li>Includes and IndexOf</li>

```js
//  Includes
const arr = [1, 2, 3, 4, 5];

arr.includes(2); //  true
arr.includes(4); //  true
arr.includes(40); //  false

//  IndexOf
let index = arr.indexOf(2); //  1
index = arr.indexOf(7); //  -1
```

<li>Slice and Splice</li>

```js
//  Slice
let arr = [1, 2, 3, 4, 5];
let arr1 = arr.slice(0, 5); //  [ 1, 2, 3, 4 ]
let arr2 = arr.slice(1); //  [ 2, 3, 4, 5 ]

//  Splice
arr = ["Ritwick", "Adam", "Mike", "Shashank"];
arr.splice(1, 2); //  [ "Ritwick", "Shashank" ]
arr = ["Ritwick", "Adam", "Mike", "Shashank"];
arr.splice(1, 2, "Aakash"); //  [ "Ritwick", "Aakash", "Shashank" ]
```

<li>Sorting</li>

```js
let arr = ["Ritwick", "Adam", "Mike", "Shashank"];
arr.sort(); // [ "Adam", "Mike", "Ritwick", "Shashank" ]
arr = [1, 2, 4, 5, 10, 100, 1000, 40];
arr.sort(); // [ 1, 10, 100, 1000, 2, 3, 4, 40, 5 ]

// But we expected, [ 1, 2, 3, 4, 5, 10, 40, 100, 1000 ]
// Why are we getting such a weird output?
// Because, the method converts the items to strings

// Solution to this problem!
function compare(n1, n2) {
  // if (n1 is less than n2) return -1;
  // else if(n1 is greater than n2) return 1;
  // else return 0;
  if (n1 < n2) return -1;
  else if (n1 > n2) return 1;
  else return 0;
}

arr.sort(function funct(a, b) {
  return compare(a, b);
}); //  [ 1, 2, 4, 5, 10, 40, 100, 1000 ]

//  It's a bit lengthy, let's make it better
arr = [1, 2, 4, 5, 10, 100, 1000, 40];
arr.sort(function (a, b) {
  return a - b;
}); //  [ 1, 2, 4, 5, 10, 40, 100, 1000 ]

//  It's much better. But, we can use `Arrow Functions` to make our code much better
arr = [1, 2, 4, 5, 10, 100, 1000, 40];
arr.sort((a, b) => {
  return a - b;
}); //  [ 1, 2, 4, 5, 10, 40, 100, 1000 ]
```

<li>Reverse and Join</li>
</ul>

**Objects - Core of JS**

<ul>
<li>Objects and its operations</li>
</ul>

**Loops**

<ul>
<li>For, While, Do while</li>
<li>Infinity Loops</li>
<li>Break and Continue</li>
<li>For...Of, For...In, ForEach</li>
</ul>

**Functions**

<ul>
<li>Arguments and Parameters</li>
<li>Return Statement</li>
</ul>
