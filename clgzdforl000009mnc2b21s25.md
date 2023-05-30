---
title: "Demystifying the State Hook"
seoTitle: "Use State Hook"
seoDescription: "React State is one of the key features of the React library, which is widely used in modern web development."
datePublished: Thu Apr 27 2023 17:00:46 GMT+0000 (Coordinated Universal Time)
cuid: clgzdforl000009mnc2b21s25
slug: demystifying-the-state-hook
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682651810680/04823165-3373-46e4-a807-20bc13c302b7.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682651832190/32e97018-e96e-4439-be57-ab7b907e761a.png
tags: web-development, webdev, reactjs, hashnode, frontend-development

---

## Introduction:

React State is one of the key features of the React library, which is widely used in modern web development. React State is a JavaScript object that represents the current state of a component. It is used to manage and update the contents of a component dynamically, based on user input or other events. Every component has a built-in state. The state is where you store the value that belongs to the component.

## Event handling

When you make a web application or any other product for a user, there will be features that are triggered. For example, the TV remote you use has buttons on it. Whenever you press a button on that remote, say volume increase, it increases the volume. So, the volume button triggered an event that increased the volume.

If you check the code below, it does a similar thing. When a button is clicked, the function handleClick is called and the "Button is clicked" is printed onto the console. An event, which is the clicking of the button has occurred and on the occurrence of that event, the handleClick function is called.

```javascript
 function Counter() {
  let count = 0;

  function handleClick() {
    console.log("Button is clicked");
  }

  return (
    <button onClick={handleClick}>
      You pressed me {count} times
    </button>
  );
}
export default Counter
```

What if you need to pass arguments into the function when the button is clicked? You cannot directly send it as `<button onClick={handleClick(10)}>` .

```javascript
 function Counter() {
  let count = 0;

  function handleClick(count) {
    count = count + 1;
  }

  return (
    <button onClick={() => handleClick(10)}>
      You pressed me {count} times
    </button>
  );
}
export default Counter
```

## **What are Hooks?**

Hooks are special functions that let you **"hook into"** various React features within functional components. These hooks make certain features like working with data fun.

## Changing the state using Use State Hook

But the problem with the above approaches is that the value of the count is being changed but the component is not being rerendered. So, the value of the counter will still be displayed as 0 on the webpage. When the component state is changed, then part of the component needs to be re-rendered. Therefore, the need for a UseState Hook arises.

`useState` is a React Hook that lets you add a [state variable](https://react.dev/learn/state-a-components-memory) to your component.

```javascript
const [state, setState] = useState(initialState);
```

## Implementing a simple counter

```javascript
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  function increment() {
    setCount(count + 1);
  }
    function decrement(){
    setCount(count -1);
  }

  return (
    <div>
        <h1>Value of a is : {count} </h1>
        <button onClick = {increment}> + </button>
        <button onClick = {decrement}> - </button>
    </div>
  );
}
export default Counter;
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681708624372/0513e83f-232a-4727-b874-b5b6864cce96.png align="center")

## Changing the state of an Object

Consider an object containing user details. When you use, `...objectname` , the previous properties of the object remain the same and you can mention the property you want to change and assign the value.

Consider a user object with a first name, last name and email address. You can modify the first name by:

```javascript
setUser({...user,firstName: "Shalini"});
```

```javascript
import { useState } from 'react';

function UserDetails() {
  const [user, setUser] = useState({
    firstName: '',
    lastName: '',
    email: '',
  });

  return (
    <>
      <label>
        First name:
        <input
          value={user.firstName}
          onChange={e => {
            setUser({
              ...user,
              firstName: e.target.value
            });
          }}
        />
      </label>
      <label>
        Last name:
        <input
          value={user.lastName}
          onChange={e => {
            setUser({
              ...user,
              lastName: e.target.value
            });
          }}
        />
      </label>
      <label>
        Email:
        <input
          value={user.email}
          onChange={e => {
            setUser({
              ...user,
              email: e.target.value
            });
          }}
        />
      </label>
      <p>
        {user.firstName}{' '}
        {user.lastName}{' '}
        ({user.email})
      </p>
    </>
  );
}
export default UserDetails
```

The above example is the one that prints the user details onto the screen as the details are being entered into the form. `onChange` method gets triggered whenever the value in the input field is changed, which triggers the setUser function which sets the values of the user object.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682612923229/17acb955-ffec-4727-b479-7f5df24dbd97.png align="center")

The react documentation has really good examples with the usage of forms as well, do refer to it. Link: [useState – React](https://react.dev/reference/react/useState).

## **Important things to know when using useState()**

There are two major rules to remember when using hooks, which include `useState()` hook.

* **ONLY call** `useState()` Hooks at the top level of your component: This means that within your component, you can only call hooks at the top and not inside any function, loop, nested function, and conditions. This helps React preserve and call hooks in the same order each time a component renders.
    
    ```javascript
    // Do not do this
    if(condition){
        const [count, setCount] = useState()(0);}
    for (let index = 0; index < 25; index++)
        {let [count, setCount] = useState()(0);}
    ```
    

## Conclusion

It's worth noting that state should not be used for all data in a component. Only data that needs to be updated dynamically should be stored in the state. Other data can be passed into a component as props.

In conclusion, the state is a crucial part of React that enables dynamic rendering and interactivity in components. By managing and updating the contents of a component dynamically, React State allows us to create dynamic and engaging user interfaces. If you're working with React, it's essential to understand the basics of state and how to use it in your components.

References:

[useState – React](https://react.dev/reference/react/useState#usestate)

[useState() Hook in React - A Complete Guide | Hygraph](https://hygraph.com/blog/usestate-react)