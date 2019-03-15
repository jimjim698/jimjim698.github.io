---
layout: post
title:      "State in React"
date:       2019-03-15 03:18:52 +0000
permalink:  state_in_react
---


State in react, simply put, is component data that can change during a component's lifecycle. This differs from props that are inherited from a parent component and do not change during a component's lifecycle. The initial state is set in the constructor because the constructor is the first thing to run when the component is made and the render function, where the state will be used, is run after. When we want to change state we use the setState function rather than explicitly writing out "this.state.counter = x." The reason for this is because setState runs asynchronously. This means that the function that setState is called in will continue to run before setState assigns the state's new values. The reason for this is mainly improved performance. If state is changed multiple times in a short span, React will batch these calls and run them at once. For example, if we have a click event for a div that changes state and a child of that div is a button that also has a click event that changes state, these state changes can be batched and run at once. This saves the page from having to re-render the DOM multiple times and can keep the page interactive while state changes take place in the background. 
