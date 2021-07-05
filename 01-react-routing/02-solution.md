```jsx
// This file is named: `App.jsx` in Qualified

// SOLUTION FILE

import React from "react";
import { BrowserRouter as Router, Redirect, Route, Switch } from "react-router-dom";

import "./App.css";

import HomePage from "./components/HomePage";
import AboutPage from "./components/AboutPage";
import ProductPage from "./components/ProductPage";
import ErrorPage from "./components/ErrorPage";

const App = () => (
  <Router>
    <Switch>
      <Route exact path='/' component={HomePage} />
      <Route exact path='/about' component={AboutPage} />
      <Route exact path='/product/:type' component={ProductPage} />
      <Route component={ErrorPage} />
    </Switch>
  </Router>
);
export default App;
```

---

```jsx
// This file is named: `components/ProductPage.jsx` in Qualified

// SOLUTION FILE

import React from "react";
import { Link } from "react-router-dom";

import Nav from "./Nav";

class ProductPage extends React.Component {
  state = {
    title: "Loading..."
  };

  componentDidMount() {
    const type = this.props.match.params.type;
    let title;

    if (type === "free") title = "Free Account";
    if (type === "premium") title = "Premium Account";

    this.setState({ title });
  }

  render() {
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
