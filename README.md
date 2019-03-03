# Learning Redux

Learning Redux often feels hard. This is often compounded by the fact that it'll
be characterized as easy, or people use large, unhelpful, terms to describe it.
I believe the problem often is that we mix-up the actual implementation of Redux
with the rationale for creating Redux.

On the most fundamental level Redux provides you with a `state` object with some helpers
for accessing it and modifying properties on it (with `reducers` and `action`s).

## Setup

First, for the purposes of this exercise I recommend installing the [Quokka](https://quokkajs.com) extension for your
editor/IDE. It turns your file(s) into live, interactive, Javascript playgrounds 🙌🏻. It'll
save you a ton of time re-opening your terminal and running `node <pathToModule>`. It'll do
it for you and give you feedback inline. Yeah. Awesome. You can read up on how to use it, or I can show
you quickly, too.

**yarn**

```sh
yarn install
```

**npm**

```sh
npm install
```

## Challenge

Let's attempt to create our own implementation of Redux! Just a basic implementation will do.
Here are the criteria:

1. Your exported Redux module should have a `createStore` function
   - This function should accept a `reducer`
   - The result of this function should be assigned to a `store` variable
2. `store` should have two helper functions `getState` and `dispatch`
   - `getState` should return the value of the current `state`.
   - `dispatch` should accept an `action` that results in the `state` being updated.
3. Write at least one meaningful test for your implementation.
   - Tests are, in essence, a form of documentation. Ask yourself, "What would be valuable
     for me to know when I'm using this in the future?"
   - Tests can be run with the `yarn test` or `npm test` commands, depending on whichever you're using.
