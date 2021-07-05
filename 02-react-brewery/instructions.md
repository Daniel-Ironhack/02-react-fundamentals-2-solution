# React Brewery

<br>

## Context

We have learned how to establish a connection between React app and the 3rd party APIs and to _get_ the data that we can display in our client app. Now, let's apply all of the concepts we have just learned and create a simple React app that uses the data from the [Brewery API](https://api.openbrewerydb.org/) to display the list of breweries.

<br>

## Getting Started

All your work should be done only in the `BreweryList.jsx` file.
More specifically, your task is to **make an `axios` request from the `componentDidMount()`** method and **save the data in the `state`** of the component `BreweryList`.

File `App.jsx` is already provided for you in the `/src` folder. `App.jsx` file already includes all the setup needed and is set as _read-only_.

<br>

To begin working, you just need to start writing your code inside the `BreweryList.jsx` file.

<br>

## Tasks & Objectives

Your task is to finish implementing the component `BreweryList.jsx`. The component already includes the basic structure.

<br>

<hr>

### Task 1: Get data from the API

⠀⠀

The goal of the task is to make an `axios` request to the [Brewery API](https://api.openbrewerydb.org/) and save the response data in the `state` of the `BreweryList`.
To do this you will need to add a `componentDidMount()` method to the component.

There is one additional constraint in this task: You will need to use the `async`/`await` syntax for the `componentDidMount()`, instead of Promises. Don't worry, to help you to get started we included the following snippet on how to do it:

**Example:**

```js
async componentDidMount () {
  try {
    // Make the `axios` request, using `await`
  } catch(error){
    // Handle the error
  }
}
```

There are a couple of requirements here, so make sure to go over the task instructions below for additional details :point_down:.

<br>

⠀

**_Tasks: `BreweryList` component_**

- Should be a class component.
- Should have a `state` with the initial value: `{ breweries: [ ] }` .
- Should have a `componentDidMount()` method.

  > As mentioned before, here you must use `async`/`await` with `componentDidMount`,
  > as in the above example.

- Should make an `axios` GET request to the BreweryAPI URL:

  > ```bash
  > # list of all breweries
  > https://api.openbrewerydb.org/breweries
  > ```

- Should set the _response_ _data_ from the BreweryAPI to the state property `breweries`.

<br>

<hr>

### Task 2: Render the list of breweries

⠀

The goal of this task is to render a simple list using the data that you got from the [Brewery API](https://api.openbrewerydb.org/) and that you finished setting in the `state` property `breweries`.

<br>⠀

**_Tasks - `BreweryList` component:_**

- Should render a list with the names of **all** the breweries.

  For each brewery create a `<div className="brewery"> </div>`, containing the brewery `name` between the tags.

  > Example:
  >
  > ```jsx
  > <div className='brewery'>
  >   <p> {/* BREWERY NAME */} </p>
  > </div>
  > ```

- **_Hint:_** Each _brewery_ object has the following structure:

  > ```js
  >   {
  >     "id": 8034,
  >     "name": "10-56 Brewing Company",
  >     "brewery_type": "micro",
  >     "street": "400 Brown Cir",
  >     "city": "Knox",
  >     "state": "Indiana",
  >     "country": "United States",
  >     "website_url": null,
  >     // ...
  >     //		... more rows
  >   }
  > ```

<br>

## Your code and submission

To check on your progress and if you are passing the tests, you can click on the **`RUN TESTS`** button.

In addition to this, you can reference the tests by opening the `__tests__/BreweryList.test.jsx` file.

**_Reminder_**: You may want to reference the test output (in the `Run Output` panel) since there might be some edge cases stated in the tests, that might not be too obvious from the instructions.

<br>

#### Final Submission

While taking the challenge, you can check your progress multiple times via the **`RUN TESTS`** button.

To submit your work, you should click on the **`SUBMIT`** button. You will be asked to review your code and make a final submission. After you are done with the final submission you won't be able to resubmit your code again.

<br>

Good luck!

_Your Ironhack team_
