---
title: "Conditional Statements and Loops in JavaScript"
seoTitle: "Conditional Statements and Loops in JavaScript"
seoDescription: "Conditional statements and loops explained in JavaScript."
datePublished: Wed Apr 05 2023 06:13:19 GMT+0000 (Coordinated Universal Time)
cuid: clg3ambj1000309mx3lgx4yk1
slug: conditional-statements-and-loops-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682796432769/b1aa287a-0e9e-4e79-8c87-94e040ab853c.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682796524053/1ea2f339-1689-4814-b761-6dafeae433de.png
tags: programming-blogs, javascript, web-development, webdev, frontend-development

---

## Introduction

Conditional statements are an essential component of any programming language, and JavaScript is no exception. They allow us to control the flow of our code based on certain conditions, enabling us to build more sophisticated and dynamic user experiences.

## if Statement

It evaluates a condition and executes the code specified in the block if the condition is true. The syntax for the `if` statement is as follows:

```javascript
if (condition) {
  // Code to be executed if condition is true
}
```

Let's look at a simple example:

```javascript
let num = 30;
if (num >= 20) {
  console.log("Conditions satisfied.");
}
```

Since `num` is greater than 20, the condition is true and "Condition satisfied" is printed onto the console.

## else Statement

We use `else` statement when we want to execute some other block of code in case the if statement is false.The syntax for the `else` statement is as follows:

```javascript
if (condition) {
  // Code to be executed if condition is true
} else {
  // Code to be executed if condition is false
}
```

Let's look at a simple example:

```javascript
let num = 10;
if (num >= 20) {
  console.log("Condition satisfied.");
} else {
  console.log("Condition not satisfied.");
}
```

If the `num` variable is less than 20, then the message "Condition not satisfied" will be logged to the console.

## else if ladder

We can also chain multiple conditions together using `else if` statements. This allows us to test multiple conditions and execute different blocks of code depending on the outcome.

The syntax for the `else if` statement is as follows:

```javascript
if (condition1) {
  // Code to be executed if condition1 is true
} else if (condition2) {
  // Code to be executed if condition2 is true
} else {
  // Code to be executed if all conditions are false
}
```

```javascript
var temperature = 25;

if (temperature > 30) {
  console.log("It's too hot!");
} else if (temperature < 10) {
  console.log("It's too cold!");
} else {
  console.log("It's just right.");
}
```

## Ternary Operator

The ternary operator is a shorthand way of writing an `if` statement in a single line. It can be useful for simple conditions that only require simple statements to be executed.

The syntax for the ternary operator is as follows:

```javascript
condition ? true_statement : false_statement;
```

Let's look at an example:

```javascript
let num = 20;
let result = (num >= 20) ? "Condition Satisfied." : "Condition not Satisfied.";
console.log(result);
```

In this example, the conditional operator checks if the `num` variable is greater than or equal to 20. If it is, the message "Condition Satisfied" is assigned to the `result` else "Condition not Satisfied." is assigned. The message is then logged onto the console.

## Switch statement

The switch statement can replace multiple if-else statements. The syntax for the Switch case is as follows:

```javascript
switch(x){
    case 'value1': { /*statements*/} break;
    case 'value2': { /*statements*/} break;
    case 'value3': { /*statements*/} break;
    default:  { /*statements*/} break;
}
```

Grouping of cases: You can do this if you want to execute the same block of code for many case statements in the switch.

```javascript
switch(x){
    case 'value1': { /*statements*/} break;
    case 'value2': // grouped two cases
    case 'value3': { /*statements*/} break;
    default:  { /*statements*/} break;
}
```

## Loops in JavaScript

Loops can be used when you want to execute a block of code repeatedly. They are used to iterate over arrays, manipulate the DOM, and perform various other tasks in web development.

## for Loop

The most common type of loop in JavaScript is the `for` loop. It is used to iterate over an array or perform an action a fixed number of times.

The syntax for a `for` loop is as follows:

```javascript
for (initialization; condition; increment/decrement) {
  // Code to be executed
}
```

Let's look at an example that prints the numbers 0 through 9 to the console:

```javascript
for (let i = 0; i < 20; i++) {
  console.log(i);
}
```

In this example, the `for` loop initializes the `i` variable to 0, then checks if it is less than 10. If `i` is less than 20, the code in the loop is executed, which logs the current value of `i` to the console. The `i` variable is then incremented by 1 and the condition is checked again. This process continues until `i` is no longer less than 20.

There are two variations of `for` loop. The `for..in` loop and `for..of` loop. `for..in` is used to iterate over the object properties whereas `for..of` is used for looping over iterables like arrays. This will be covered in a later blog after objects are introduced.

## while Loop

The `while` loop is another loop that executes the code as long as the specified condition is true. The syntax for a `while` loop is as follows:

```javascript
while (condition) {
  // Code to be executed
}
```

Let's look at the same example using a while loop:

```javascript
let i = 0;
while(i < 20){
    console.log(i);
    i += 1;
}
```

### do...while Loop

The `do...while` loop is similar to the `while` loop, but it executes the code at least once before checking the specified condition. The syntax for a `do...while` loop is as follows:

```javascript
do {
  // Code to be executed
} while (condition);
```

Let's look at an example that asks the user to enter a number between 1 and 100 until a valid number is entered:

```javascript
let i = 0;
do {
  console.log(i);
} while (i < 10);
```

## Which loop to use?

* Use for loop when you know the number of iterations you will be performing or when you need to loop through the array.
    
* Use while loop when you need to run the loop till a particular condition is false but you don't know the exact number of iterations.
    

## Break and continue

You can exit the loop when you want, using a break statement (even if the condition isn't false).

```javascript
n = 1;
while(true){
    if(n == 5) break;
    n += 1;
}
```

Use continue if you don't want the code to execute for that particular iteration.

```javascript
n = 1;
while(n < 7){
    if(n == 5) continue;
    n += 1;
}
```

### Conclusion

By mastering conditional statements, we can create more sophisticated and dynamic user experiences. Loops in JavaScript provide a powerful tool for iterating over arrays, generating random numbers, and performing various other tasks in web development. By mastering the `for`, `while`, and `do...while` loops, we can create more sophisticated and dynamic web applications.