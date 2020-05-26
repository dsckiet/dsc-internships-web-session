*Types*

**Primitives**

<ul>
  <li>String</li>
  <li>Number</li>
  <li>Boolean</li>
  <li>null</li>
  <li>undefined</li>
  <li>Symbol</li>
<ul>

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
  console.log("Hello " + ${name} + "!");
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
