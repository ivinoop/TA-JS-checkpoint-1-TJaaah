1. Using loops take 10 inputs from user and find the average of all the numbers.

```js
  let prevValue = 0;
  for (let i = 1; i <= 10; i++) {
  let input = +prompt('Enter a number');
  prevValue += input ;
  }
  console.log(`Sum of all inputs is ${prevValue}`);
  let avg = prevValue / 10;
  console.log(`Average is ${avg}`); 
```

2. What will be the output of the code below

```js
let i = 0;
while (i < 3) {
  alert('hi');
  i++;
}
```

Ans: Output will be `hi` printed 3 times until the value of `i` is less than 3.


3. Write a function named `getEvenSum` that accepts a parameter `max`. Return the sum of all even numbers. The value of max should default to 10.

```js
function getEvenSum(max = 10) {
  let evenSum = 0;
  for (let i = 0; i <= max; i++) {
    if(i % 2 == 0) {
      evenSum += i;
    }
  }
  return `The sum of even numbers is ${evenSum}`;
}
```

4. Write a function named `getOddSum` that accepts a parameter `max`. Return the sum of all odd numbers. The value of max should default to 10.

```js
function getOddSum(max = 10) {
  let oddSum = 0;
  for (let i = 0; i <= max; i++) {
    if(i % 2 !== 0) {
      oddSum += i;
    }
  }
  return `The sum of odd numbers is ${oddSum}`;
}
```

5. Write a function named `getProductOfDigits` that accepts a parameter `num`. It returns the product of all the digits in the number.

- If the input value is less than 0 return `not a valid input`
- For example if the input is `123` output should be `6`.

```js
function getProdcutOfDigits(num) {
  let prod = 1;
  while(num > 0) {
    prod = prod * (num % 10);
    num = Math.floor(num / 10);
  }
  return prod;
}
```

6. What will be the output of the following code below in multiple conditions? Explain with reason?

```js
function check(num) {
  if (num > 5) {
    return 'Bigger than 5';
  }

  if (num < 5) {
    return 'Smaller than 5';
  }

  return num;
}

check(10); // Bigger than 5
check(1); // Smaller than 5
check(5); // 5
```

7. What will be the output of the following code given below? Explain the reason?

```js
function getOutput(name) {
  if (name === 'Arya') return 'You are arya';
  if (name === 'John') return 'You are john';
  return 'Who are you';
}

getOutput('Arya'); // You are arya
getOutput('John'); // You are john
getOutput(); // Who are you ; since no arguments are passed. 
```

8. What will be the output of the following code given below? Explain the reason?

```js
function getOutput(name) {
  if (name === 'Arya') console.log('You are arya');
  if (name === 'John') console.log('You are john');
  return 'Who are you';
}

getOutput('Arya'); // "You are arya" is the console.log() output whereas "Who are you" will be ouput returned to the function and displayed
getOutput('John'); // "You are john" is the console.log() output whereas "Who are you" will be ouput returned to the function and displayed
getOutput(); // "Who are you"
```

9. Can a function have multiple return statement? Give one example if possible and explain the reason.

Ans: Yes, a function can have multiple return statements but only the first return statement will be executed in the function execution.

Example: 

```js
function getOutput(name) {
  if (name === 'Arya') console.log('You are arya');
  if (name === 'John') console.log('You are john');
  return 'Who are you';
  return 'Vinoo';
  return 'AltCampus is great!';
}
```

In the above code segment, only the first `return` statement is executed and other two statements are not considered.


10. What is the difference between `for` loop and `while` loop. What are the different place you can use them? Explain with example.

Ans: `for` loop uses an iterative conditional statement to perform a further set of operations or expressions inside it. 

Example: Printing numbers until a maximum value is reached

```js
function printNum(num = 21) {
  for(let i = 1; i <= num; i++) {
    console.log(i);
  }
}
```

In the above example, the `for` loop iterates through from 1 to num, and prints the value on the console accordingly. `for` loops are useful in such cases of iterative conditions.

`while` loop is used to set a predefined condition, and only when it is satisfied, the statements inside it will get executed.

Example: Printing something to the console if a condition is satisfied

```js
function printName () {
  let num = +prompt(`Enter a number`);
  while (num > 5) {
    return `Hello there!`;
  }
}
```

In the above example, only if the user enters a number greater than 5, the console.log() will be executed. Otherwise, it returns `undefined`, meaning that the condition mentioned in `while` loop was not satisfied.
