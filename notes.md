GitHub usage:
- git clone link
- git pull
- git add ThingBeingAdded
- git commit -am "Commit Notes"
- git push
- git fetch
- git status
  
The Internet:
### [TCP/IP] layers

| Layer       | Example         | Purpose                               |
| ----------- | --------------- | ------------------------------------- |
| Application | HTTPS           | Functionality like web browsing       |
| Transport   | TCP             | Moving connection information packets |
| Internet    | IP              | Establishing connections              |
| Link        | Fiber, hardware | Physical connections                  |

JavaScript:
- Comments
// Line comment
/*
Block comment
*/

- Basic function
  function join(a, b) {
    return a + ' ' + b;
  }
  console.log(join('Hello', 'world'));
  // OUTPUT: Hello world

-   CSS delarations in log output
  console.log('%c JavaScript Demo', 'font-size:1.5em; color:green;');
  // OUTPUT: JavaScript Demo //in large green text

- Timers
  console.time('demo time');
  // ... some code that takes a long time.
  console.timeEnd('demo time');
  // OUTPUT: demo time: 9762.74 ms

- Counting
  console.count('a');
  // OUTPUT: a: 1
  console.count('a');
  // OUTPUT: a: 2
  console.count('b');
  // OUTPUT: b: 1

- JavaScript in HTML
  js:
  function sayHello() {
    console.log('hello');
  }

  html:
  <head>
  <script src="javascript.js"></script>
  </head>
  <body>
    <button onclick="sayHello()">Say Hello</button>
    <button onclick="sayGoodbye()">Say Goodbye</button>
    <script>
      function sayGoodbye() {
        alert('Goodbye');
      }
    </script>
  </body>

  other parts:
  <button onclick="let i=1;i++;console.log(i)">press me</button>
  <!-- OUTPUT: 2 -->

- Declaring variables:
  let - can chage value of variable
  cont - will cause error if you attempt to change it
  null - type that has not been assigned a value
  undefined - type that has not been defined
  boolean - true or false
  number - 64-bit signed number
  BigInt - number of arbitrary magnitude
  String - textual sequence of characters
  Symbol - unique value
  Object - collection of properties represented by name-value pairs. Values can be of any type ex. {a:3, b:'fish'}
  Function - object that has the ability to be called. ex. function a() {}
  Date - calendar dates and times. ex. new Date('1995-12-17')
  Array - ordered sequence of any type. ex. [3, 'fish']
  Map - collection of key-value pairs that support efficient lookups. ex. new Map()
  JSON - lightweight data-interchange format used to share information across programs. ex. {"a":3, "b":"fish"}

- Common operators:
  has all common plus concatenation and strict equality (===) and inequality (!==)

- Examples of weakly typed language: (variable type can change at any given point)
  2 + '3';
  // OUTPUT: '23'
  2 * '3';
  // OUTPUT: 6
  [2] + [3];
  // OUTPUT: '23'
  true + null;
  // OUTPUT: 1
  true + undefined;
  // OUTPUT: NaN
  1 == '1';
  // OUTPUT: true
  null == undefined;
  // OUTPUT: true
  '' == false;
  // OUTPUT: true
  1 === '1';
  // OUTPUT: false
  null === undefined;
  // OUTPUT: false
  '' === false;
  // OUTPUT: false

- Conditionals:
  if (a === 1) {
    //...
  } else if (b === 2) {
    //...
  } else {
    //...
  }

  a === 1 ? console.log(1) : console.log('not 1');

  if (true && (!false || true)) {
    //...
  }

- Loops:
  for:
  for (let i = 0; i < 2; i++) {
    console.log(i);
  }
  // OUTPUT: 0 1

  do while:
  let i = 0;
  do {
    console.log(i);
    i++;
  } while (i < 2);
  // OUTPUT: 0 1

  while:
  let i = 0;
  while (i < 2) {
    console.log(i);
    i++; 
  }
  // OUTPUT: 0 1

  for in: (iterates over an object's property names)
  const obj = { a: 1, b: 'fish' };
  for (const name in obj) {
    console.log(name);
  }
  // OUTPUT: a
  // OUTPUT: b

  (for arrays the object's name is the array index)
  const arr = ['a', 'b'];
  for (const name in arr) {
    console.log(name);
  }
  // OUTPUT: 0
  // OUTPUT: 1

  for of: (iterates over an iterable's (Array, Map, Set, ...) preperty values)
  const arr = ['a', 'b'];
  for (const val of arr) {
    console.log(val);
  }
  // OUTPUT: 'a'
  // OUTPUT: 'b'

  Break and continue: (all of the looping constructs above allow either a break or continue to abort or advance the loop)
  let i = 0;
  while (true) {
    console.log(i);
    if (i === 0) {
      i++;
      continue;
    } else {
      break;
    }
  }
  // OUTPUT: 0 1

- Strings:
  string variable is specified by surrounding a sequence of characters with ', ", or `. Single or double quotes are equivalent, but the backtick defines a string literal that may contain js that is evaluated in place and concatenated into the string. A string literal replacement specifier is declared with a dollar sign followed by a curly brace pair. Anything inside is evaluated as js. Backticks can also create multiling string without having to explicitly espace the newline character(\n).
  
  'quoted text'; // " also works
  const l = 'literal';
  console.log(`string ${l + (1 + 1)} text`);
  // OUTPUT: string literal2 text

- String Functions:
  length - number of characters in the string
  indexOf() - the starting index of a given substring
  split() - split the string into an array on the givern delimiter string
  startsWith() - true if the string has the given prefix
  endsWith() - true if the string has the given suffix
  toLowerCase() - converts all characters to lowercase

  ex.
  const s = 'Example:조선글';
  console.log(s.length);
  // OUTPUT: 11
  console.log(s.indexOf('조선글'));
  // OUTPUT: 8
  console.log(s.split(':'));
  // OUTPUT: ['Example', '조선글']
  console.log(s.startsWith('Ex'));
  // OUTPUT: true
  console.log(s.endsWith('조선글'));
  // OUTPUT: true
  console.log(s.toLowerCase());
  // OUTPUT: example:조선글
  
