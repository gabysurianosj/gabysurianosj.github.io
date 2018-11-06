---
layout: post
title:      "Developing with React and Redux"
date:       2018-11-06 13:13:35 +0000
permalink:  developing_with_react_and_redux
---

React is taking over the web as it’s currently used in countless applications. When it came out in the first place, it made everyone talk about how good it was. The Virtual Dom was a breakthrough and it took the development of applications to a whole new level. I was pretty amazed by all these cool things, so I was looking forward to using it in a project.

Here are  things I have learned about developing with React and Redux:

1. Components are important. Each component is an independent, reusable piece of code that can be used everywhere in your app. The inputs they accept are called props. As React documentation states: a component must never modify its own props. It is also highly recommended to create small components (like buttons, inputs, etc.) that can be reused in different parts of your application.

2. Organizing state can be a lot better with Redux. Managing state over time can be complex, so you need a tool like Redux to help you get through this.

![Redux advantage](https://cdn-images-1.medium.com/max/1600/1*Fg7Z41iRadjDqUQUe2bgMA.jpeg)

Its basic idea is that you store the whole state of the app in a one object tree that is kept in a single store. This state object is read-only and can be modified only by emitting an action. Actions are just plain JS objects, which are being returned by functions, called actions creators, each time a new change is about to happen. When a new action is emitted, a reducer is responsible for handling this event. Reducers are just pure functions, that take the previous state and an action, and return the next state of the app.

When implementing a React-Redux application, components get their state from the Redux store, and they send their state changes to the store as well. Every time the state changes, the components that have access to it, will update their content based on this change.

