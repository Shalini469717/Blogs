---
title: "JavaScript Functions"
seoTitle: "JavaScript Functions"
seoDescription: "How to use functions in Javascript?"
datePublished: Wed Apr 05 2023 08:42:38 GMT+0000 (Coordinated Universal Time)
cuid: clg3fyc3n000009ljfn2zawg0
slug: javascript-functions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682800858225/95871b55-4433-4d0d-bc33-80b8430e12c9.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682800872520/1cb201f5-7608-4d83-a288-44def4b86ac5.png
tags: programming, javascript, web-development, webdev, frontend-development

---

## Introduction

Functions are a fundamental building block in JavaScript.We use functions to avoid the repetition of code . When you call a function, it executes the code within the body of the function. Again, similar to the variable name, you need to have a meaningful name for your function so that the one reading the code can understand what it does without reading the entire body of the function. In this article, we'll take a closer look at JavaScript functions and their syntax.

## Defining Functions

Here's an example of how to define a function in JavaScript:

```javascript
function functionName(parameter1, parameter2, ...){
    // body of the function
    return value; // if you want the function to return a value
}
let result = functionName(p1,p2..); // calling the function
```

The function returns the value when it encounters a `return` statement. It doesn't execute further.

Function parameters are the named variables inside a function's definition. They are used to receive input values when the function is called. In the example above, `parameter1`, `parameter2`,... are the function parameters.

Function arguments, on the other hand, are the values passed to a function when it is called. In the above example, `p1` and `p2` are the arguments passed to the `functionName` function:

In ES6, we can set default values for function parameters. This means that if a user doesn't pass in a value for a certain parameter, the default value will be used instead.

```javascript
function showMessage(name, text = "hello"){
    console.log(text + name);
}
showMessage("Rob");
// output would be hello Rob
```

Never add a new line between the return statement and the value. Since javascript assumes a semicolon after return, the value won't be returned.

## Function Expressions

Function expressions are another way to define functions in JavaScript. Unlike function declarations, which are hoisted to the top of the scope, function expressions are not hoisted, meaning they cannot be called before they are defined in the code.

```javascript
let message = function(){
    return "hello";
};
message();
```

Note that there is no name after the `function` keyword. Omitting a name is allowed for a function expression.

Function Expression is created here as `function(…) {…}` inside the assignment statement: `let message = …;`. The semicolon `;` is recommended at the end of the statement, it’s not a part of the function syntax.

## Callback functions

They are functions that are passed as arguments to another function and are executed when a certain event happens.

```javascript
function check(question, correct, wrong){
    if (question == "ques") correct()
    else wrong();
}
function show(){
    console.log("ok");
}
function cancel(){
    console.log("cancelled");
}
check("ques",show,cancel);
```

**The arguments** `show` and `cancel` of `check` are called *callback functions* or just *callbacks*.

```javascript
check("ques",
function (){console.log("ok");},
function (){console.log("cancelled");}
);
```

In the above example, some functions don't have names and they are declared inside the function call. These functions are called anonymous functions.

## Arrow Functions

Arrow functions are a shorthand way of writing function expressions in JavaScript. They provide a concise syntax for writing functions.

```javascript
let myfunc = (arg1, arg2, arg3.., argx) => {/* body of the function */}
```

Example:

```javascript
let add = (num1, num2) => {
  return num1 + num2;
};
console.log(add(3, 4)); // Output: 7
```

## Conclusion

By understanding the syntax and usage of functions in JavaScript, we can become better programmers and build more powerful applications.

  
*Thank you for reading. Feel free to share any tips or resources in the comments!*