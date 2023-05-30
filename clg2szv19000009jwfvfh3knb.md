---
title: "Variables, Data Types, Operators in JavaScript"
seoTitle: "Variables, Data Types, Operators in JavaScript"
seoDescription: "Variables, Data Types, Operators in JavaScript"
datePublished: Tue Apr 04 2023 21:59:58 GMT+0000 (Coordinated Universal Time)
cuid: clg2szv19000009jwfvfh3knb
slug: variables-data-types-operators-in-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682793513603/ab9c5bff-db9a-48b3-ad82-f9b275422ea7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682793550328/1e5d0c7a-fa16-4c9f-9639-489519446506.png
tags: programming, javascript, web-development, webdev, frontend-development

---

## Introduction

When you start learning a new language, the first thing you need to learn is how to declare a variable and store values in them along with data types and basic operations. In this blog, all of these topics will be covered.

## Variable Declaration

Variables are used to store the data, they are like containers. We can create a variable in Javascript using the `let` keyword. You need not declare the data type since Javascript decides the data type by itself.

You can declare a constant by using the `const` keyword.

```javascript
let name = "Shalini"; //declare using let keyword
let num = 1;
const id = "5170496"; // declaring a constant
```

`var` and `let` are both keywords in JavaScript used for declaring variables. However, they have some differences in the way they work.

The main difference between `var` and `let` is in their scope:

1. Scope: Variables declared with `var` are function-scoped, while variables declared with `let` are block-scoped. This means that variables declared with `var` are accessible throughout the function in which they are declared, while variables declared with `let` are only accessible within the block in which they are declared (i.e., within a pair of curly braces).
    

```javascript
// Example 1 - var
function example1() {
  var x = 10;
  if (true) {
    var x = 20;
    console.log(x); // Output: 20
  }
  console.log(x); // Output: 20
}

example1();

// Example 2 - let
function example2() {
  let y = 10;
  if (true) {
    let y = 20;
    console.log(y); // Output: 20
  }
  console.log(y); // Output: 10
}

example2();
```

1. Hoisting: Variables declared with `var` are hoisted to the top of the function (or global) scope, which means they can be used before they are declared. Variables declared with `let` are not hoisted and will throw a ReferenceError if they are used before they are declared.
    

```javascript
console.log(a); //Output: undefined
var a = 5;

console.log(b); // ReferenceError: b is not defined
let b = 10;
```

In summary, the main differences between `var` and `let` in JavaScript are their scoping rules and hoisting behavior. Variables declared with `var` are function-scoped and hoisted, while variables declared with `let` are block-scoped and not hoisted.

## Variable Naming

A variable name can contain letters, digits and \_,$ but it must not start with a digit. Camel casing can be used if it contains multiple words. The name is case-sensitive and doesn't use reserved words such as "class", "return", "let" etc.

Though you can name your variables according to your liking, it is always a good practice to give them a meaningful name. This way the code is more readable.

## Data Types

1. Number: both integers and floating point numbers. NaN stands for not a number. It represents a computational error. It is a result of an incorrect or undefined mathematical operation. Any further mathematical operations with NaN return NaN.
    
2. String: It is represented by quotes. There is no character type.
    
    ```javascript
    let str = "Hello";
    let str2 = 'Single quotes are ok too';
    let phrase = `can embed another ${str}`;
    ```
    
3. Boolean: It has only two values true or false.
    
4. `null` is used to assign an empty or unknown value to the variable and `undefined` is the default initial value for undefined things. They are not data types.
    

## Basic Operators

* Addition `+`,
    
* Subtraction `-`,
    
* Multiplication `*`,
    
* Division `/`,
    
* Remainder `%`,
    
* Exponentiation `**`
    
* Assignment `=`
    
* Increment and Decrement `++` , `--`
    
* Comparison `==` is equal to but doesn't check the data type, `===` is equal to and checks the datatype. `<= >= !=` are other comparison operators.
    
* Bitwise Operators `| & ^ ~ << >>`
    
* Conditional `?:`
    
* Logical `&& || != ==`
    

References: [JavaScript Fundamentals](https://javascript.info/first-steps)