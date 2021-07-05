# React Routing

<br>

## Context

We have learned how to set up _React Router_ and create _routes_ that could render different components. Additionally, we learned how to use [URL parameters](https://medium.com/@tylermcginnis/url-parameters-with-react-router-fc58cb2c37bd) to set and access dynamic segments of the URL. In this exercise, you will have a chance to check your understanding of _React Router_ and being able to set up basic routing for a React app.

<br>

## Getting Started

All your work should be done in the files `App.jsx` and `ProductPage.jsx`.
More specifically, **your task is to set up `<Route>`s in `App.jsx`** and to **access URL parameters in the `ProductPage.jsx`**.

Following components are already provided for you in the `/src` folder ( \*you don't need to implement them, they are **read-only\***):
`HomePage.jsx` , `AboutPage.jsx`, `ErrorPage.jsx` and `Nav.jsx`.

Files `App.jsx` and `ProductPage.jsx` already include the React app setup that you will need.

<br>

To begin working, you just need to start writing your code inside the `App.jsx` and `ProductPage.jsx` files respectively for each task.

<br>

## Task & Objectives

Your first task is to add _React Router_ `<Route>`s in `App.jsx` that render page components correctly.
Second, you will need to implement `componentDidMount()` lifecycle method in the `ProductPage.jsx` and update the `state` depending on the text of the URL parameter.

Do not worry about the styles, the main point of the exercise is to create the components following the task requirements.

<br>

<hr>

### 1. Add the `<Route>`s to `App.jsx`

File `App.jsx` already contains one `Route` with the `path="/"` for the `HomePage` component.
Your task is to implement the full React routing by adding 3 more `Route`s for the page components `AboutPage`, `ProductPage` and `ErrorPage`.

**Hint**: Feel free to consult React's [documentation on passing children elements](https://reactjs.org/docs/composition-vs-inheritance.html) and the use of the [special `children` prop](https://reactjs.org/docs/glossary.html#propschildren) if you get stuck.

<br>

**Tasks** - **_`App` component:_**

- should have a `Route` with `path="/about"` , for `AboutPage` component.
- should have a `Route` with `path="/product/:type"` , for `ProductPage` component.

  > Notice that this `Route` has a URL parameter `:type`, that you will use in the _Task 2_.

- should have a `Route` _without_ a `path` that by default renders the `ErrorPage` component, on a bad URL that doesn't match any existing `Route`.

###### Example:

![](https://i.imgur.com/EaY9F2j.png)

<br>

<hr>

### 2. Access URL params and update `state` of `ProductPage`

In this task, you will work in the `ProductPage.jsx` file.

The `ProductPage` already includes the component structure, the `state`, and the `render()` method.

You **shouldn't change** anything in the `state` and `render`.

When a link **Free** or **Premium** is clicked on the `HomePage`, the _URL_ changes to either `/product/free` or `/product/premium` depending on the button clicked and `ProductPage` is displayed.

<!-- ![](https://media3.giphy.com/media/R0pQnMtN3pGkQCbMAb/giphy.gif)  -->

<br>

![](https://media2.giphy.com/media/MxJC3SSrBHdPiV5UuD/giphy.gif)

Your task is to get the dynamic part of the URL (_URL parameter_) `/free` or `/premium ` and update the `title` property in the `state`.

<br>

**Tasks - `ProductPage`component**

- Should have a `componentDidMount()` method,
- In the `componentDidMount()`:
  - should set _state_ `title` to `"Premium Account"` when URL is `"/product/premium"`.
  - should set _state_ `title` to `"Free Account"` when URL is `"/product/free"`.

<br>

**Hint**: Feel free to check [this example](https://ui.dev/react-router-v4-pass-props-to-link/) on how to access URL parameters, if you get stuck.

<br>

<hr>

<br>

**Hint**: Make sure to also check the test results and the description provided in the **`Run Output`** section for additional details. Sometimes merely wrong spelling can lead to failing tests so make sure you always check the tests.

<br>

## Your code and submission

To check on your progress and if you are passing the tests, you can click on the **`RUN TESTS`** button.

In addition to this, you can reference the tests by opening the files `__tests__/App.test.jsx`.

**_Reminder_**: You may want to reference the test output (in the `Run Output` panel) since there might be some edge cases stated in the tests, that might not be too obvious from the instructions.

<br>

#### Final Submission

While taking the challenge, you can check your progress multiple times via the **`RUN TESTS`** button.

To submit your work, you should click on the **`SUBMIT`** button. You will be asked to review your code and make a final submission. After you are done with the final submission you won't be able to resubmit your code again.

<br>

Good luck!

_Your Ironhack team_
