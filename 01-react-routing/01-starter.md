- The public URL to the assessment: https://www.qualified.io/assess/608139c5d81046001217c89e

```jsx
// This file is named: `App.jsx` in Qualified

import React from "react";
import { BrowserRouter as Router, Redirect, Route, Switch } from "react-router-dom";

import "./App.css";

import HomePage from "./components/HomePage";
import AboutPage from "./components/AboutPage";
import ProductPage from "./components/ProductPage";
import ErrorPage from "./components/ErrorPage";

// Do not modify the above code.

const App = () => (
  <Browser>
    <Switch>
      <Route path='/' component={HomePage} />

      {/*Task 1.1: create Route `/about` for `AboutPage` component */}

      {/*Task 1.2: create Route `/product/:type` for `ProductPage` component */}

      {/*Task 1.3: create Route without `path` that renders `ErrorPage` on a bad URL `/` */}
    </Switch>
  </Browser>
);
export default App;
```

---

```jsx
// This file is named: `components/ProductPage.jsx` in Qualified

import React from "react";
import Nav from "./Nav";

class ProductPage extends React.Component {
  state = {
    title: "Loading..."
  };

  // YOUR CODE HERE

  render() {
    /* DO NOT CHANGE ANY OF THE CODE IN THE `render()`. 
     ALL OF YOUR WORK SHOULD BE DONE INSIDE `componentDidMount()`` 
     WHERE INDICATED ABOVE BY THE COMMENT `// YOUR CODE HERE`
    */
    return (
      <div id='main'>
        <Nav />

        <h2>Product Page</h2>

        <p>{this.state.title}</p>
      </div>
    );
  }
}

export default ProductPage;
```

---

```jsx
// This file is named: `components/AboutPage.jsx` in Qualified

// No changes will be done in this file

import React from "react";
import Nav from "./Nav";

const AboutPage = () => {
  return (
    <div id='main'>
      <Nav />
      This is the About page.
    </div>
  );
};

export default AboutPage;
```

---

```jsx
// This file is named: `components/ErrorPage.jsx` in Qualified

// No changes will be done in this file

import React from "react";
import Nav from "./Nav";

const ErrorPage = () => {
  return (
    <div id='main'>
      <Nav />
      Page Not Found!
    </div>
  );
};

export default ErrorPage;
```

---

```jsx
// This file is named: `components/HomePage.jsx` in Qualified

// No changes will be done in this file

import React from "react";
import { Link } from "react-router-dom";

import Nav from "./Nav";

const Home = () => {
  return (
    <div id='main'>
      <Nav />
      Welcome to the Home page!
      <br />
      <Link to='/product/free'>
        {" "}
        <button>Free</button>{" "}
      </Link>
      <br />
      <Link to='/product/premium'>
        {" "}
        <button>Premium</button>{" "}
      </Link>
    </div>
  );
};

export default Home;
```

---

```jsx
// This file is named: `components/Nav.jsx` in Qualified

// No changes will be done in this file

import React, { useState } from "react";
import { Link } from "react-router-dom";

import "./Nav.css";

const Nav = () => {
  return (
    <nav>
      <Link to='/'>Home</Link>
      <Link to='/about'>About</Link>
    </nav>
  );
};

export default Nav;
```
