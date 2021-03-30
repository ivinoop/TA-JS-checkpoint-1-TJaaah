1. What is the difference between the two `sum` function given below?

```js
// first
function sum(a, b) {
  return a + b;
}

// second
function sum(a, b) {
  console.log(a + b);
}
```
Ans:

In the first function, a + b is returned as a value to the function. In the second function, console.log() is used to print the result of a + b on the console.


2. If we store the returned value of both functions above in variable `first` and `second` what will be the value of `first` and `second`.

Ans:

Return values cannot be stored in a variable, so the output would be an error message.

3. What will be the output when you call above `sum` function (first) with three parameter like `sum(12, 24, 35)`. Explain why?

Ans:

The output will be 36, since only the first two parameters are considered and the third parameter is discarded since there is no corresponding argument for it.


4. Can you store the first `sum` function in a variable named `add`. If yes why? If no why?

Ans:

Yes, the function can be stored in a variable since a function is an expression and not a statement.

5. Declare a function named `sayHello` the accepts a parameter `name` and returns the name like `Hello Arya`.

Ans:

```js
function sayHello(name) {
  return `Hello Arya`;
}
```

6. What will be the output of the function below and why?

```js
let userName = 'John';

function showMessage() {
  let message = 'Hello, ' + userName;
  return message;
}

showMessage();
```

Ans:

Output of above code will be `Hello, John` since the variable userName is assigned the value of "John" and the variable `message` has the concatenation expression.


7. What will be the output for `Output1` `Output2` and `Output3` in the code below.

```js
let userName = 'John';

function showMessage() {
  let message = 'Hello, ' + userName;
  return message;
}

alert(userName); // John

showMessage(); // Hello, John

alert(userName); // John
```

8. What is a Anonymous Function give example of three functions.

Ans: 

A function that is defined without a name while being stored in a variable, is called an Anonymous function. To access / call the function again, the variable name is used.

Example 1:

```js
let anonFunc = function () {
  alert `This is an anonymous function`;
}

anonFunc();
```

Example 2:

```js
let add = function(a,b) {
  return a + b;
}

add(39,22);
```

Example 3:

```js
let isVoter = function(age) {
  if (age > 18) {
    return `You are a voter`;
  } else {
    return `Register as a voter today!`;
  }
}

isVoter(45);
```

9. Can function declaration be a Anonymous Function? Explain

Ans: No, since Anonmyous functions are always invoked with the variable name they were defined under, they have to defined too, and not just declared.

10. Give 5 example of good naming convention for defining a function. You can read the details below to do that.

```md
Functions are actions. So their name is usually a verb. It should be brief, as accurate as possible and describe what the function does, so that someone reading the code gets an indication of what the function does.

It is a widespread practice to start a function with a verbal prefix which vaguely describes the action. There must be an agreement within the team on the meaning of the prefixes.

For instance, functions that start with "show" usually show something.

Function starting with…

"get…" – return a value,
"calc…" – calculate something,
"create…" – create something,
"check…" – check something and return a boolean, etc.
```

Ans:

1. camelCase

Using camelCase is a good naming convention for function declaration/definition. In complex code bases, there are innumerable functions, so naming them without context would be very confusing. camelCase naming helps a lot. 

Example: 
```js
function showOptions() {
  //code
}
```

Here, showOptions() is a function that is easily understandable meaning that it shows a few options to the user when clicked on, or when some other trigger happens. The naming starts with lower-case and then has an upper-case alphabet in the middle. This helps in reading very long function names, easily.

2. Proper Names

Names that immediately tell the user what functionality a function performs. 

Example:
```js
function isGreater(a,b) {
  return a > b;
}
```

Here, the obvious answer would be a YES or NO. Or, in terms of programming, TRUE or FALSE. So, a function name that appropriately describes this functionality is a good convention to follow.

3. Spaces between operators

To make the code look neat and readable, spaces must be used wherever operators and variables are used.

Example:

```js
function printSum(numA) {
  let sum = 0;
  for(let i = 0; i <= numA; i++) {   // Spaces between operators in for loop
    sum += i;
  }
return sum;
}
```