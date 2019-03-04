# Learning Redux

Learning Redux often feels hard. This is often compounded by the fact that it'll
be characterized as easy, or people use large, unhelpful, terms to describe it.
I believe the problem often is that we mix-up the actual implementation of Redux
with the rationale for creating Redux. It's just a little to Computer Science-y for
the rest of us.

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

Attempt to create your own implementation of Redux! Just a basic implementation will do.
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

---

### Yearning for more?

Now that you have a Redux of your very own, use it. This means that you'll need to create
your own way of implementing Redux into our app. Remember, Redux is framework/library agnostic
it can be used in an Angular 5+, Vue (although you'd probably use [Vuex](https://vuex.vuejs.org/), instead), or whatevs.

Essentially, you'll need to create your own implementation of React Redux (but wayyyyy lighter). This means you'll need:

1. A way to integrate your newly created `store` into your app.
   - The [documentation](https://react-redux.js.org/introduction/quick-start) might be a good place to start
   - Familiarizing yourself with [context](https://reactjs.org/docs/context.html) within a React app will probably help, too.
2. A way to access/update properties on `state` within a component (i.e. `mapStateToProps` and `mapDispatchToProps`).
   - We typically do this with the `connect` module from React Redux.
3. Write a handful of tests for your new component.
   - Validate that `state` changes
   - Ensure that your component re-renders.
   - Is there anything more of value that you think a test could provide?

---

### [Lasciate ogne speranza, voi ch'intrate](<https://en.wikipedia.org/wiki/Inferno_(Dante)#Vestibule_of_Hell>)

If you chose an HOC pattern for your `connect` function, attempt to create
a solution that uses the new Hooks API.

Beware, that this is new ground for us all. React Redux doesn't even have an API for this, yet. You'd be treading new ground, which means you'll be largely alone. Apart from us, of course 🙂.

This may, but not necessarily, mean your tests break. I'm sure we'll all be far too impressed with what you've done to care.
