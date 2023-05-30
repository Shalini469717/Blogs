---
title: "Basics of JavaScript"
seoTitle: "Basics of JavaScript"
seoDescription: "Learn about some basic rules and how to add JavaScript to your code"
datePublished: Tue Apr 04 2023 21:13:04 GMT+0000 (Coordinated Universal Time)
cuid: clg2rbjyb000109jx66qb30sw
slug: basics-of-javascript
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682769635655/9424ed53-f095-48bd-9461-efee42afc380.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682769653022/0be55642-cf01-4cee-880c-6f8ea148e94f.png
tags: programming, javascript, web-development, frontend-development

---

## Introduction

In this blog, you will be learning about basics of Javascript i.e. how you can add JavaScript to your code and what are some of the rules to be followed.

## Adding JavaScript to your code

You can add JavaScript to your code in various ways:

1. You can use the &lt;script&gt;&lt;/script&gt; tags in the HTML file itself to insert the javascript code.
    

```javascript
<script> alert("Hello"); </script>
```

1. If you have a lot of Javascript code then you might consider creating a javascript file and add to the HTML file at the bottom of the HTML code. Let us name the newly created JavaScript file as "app.js". Then you need to the following code in "index.html".
    

```javascript
<script src = "./app.js"></script>
```

Since you are adding a file, if any code is written in between the script tags, it will be ignored.

1. You can consider doing it as a combination of both the above methods too.
    

```javascript
<script src = "./app.js"></script>
<script> alert("Hello");</script> 
```

You can add multiple files too!

```javascript
<script src = "./script1"></script>
<script src = "./script2"></script2>
```

I prefer adding it in a different file and the code is not too cluttered.

## Code Structure

1. Statements: These are the building blocks of the code. Each line in the javascript code is a statement. They are usually written in separate lines to make the code more readable.
    
2. Semicolons: It is your choice to add the semicolon at the end or not. Syntactically, it doesn't produce any errors. But there might be a problem in cases such as these when the semicolon is not used.
    
    ```javascript
    alert("Hello")
    [1,2,43].forEach(alert);
    ```
    
    Javascript interprets the above code as :
    
    ```javascript
    alert("Hello")[1,2,43].forEach(alert);
    ```
    
    It produces an error. So it is better to add a semicolon at the end.
    
3. Comments: Single line comment and multiline comment
    
    ```javascript
    // this is a single line comment
    /* this 
    is a multiline
    comment */
    ```
    
    References :  
    [JavaScript Fundamentals](https://javascript.info/first-steps)