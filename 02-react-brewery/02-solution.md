```jsx
// This file is named: `BreweryList.jsx` in Qualified

// SOLUTION FILE

import React, { Component } from "react";
import axios from "axios";

class BreweryList extends Component {
  state = {
    breweries: []
  };

  async componentDidMount() {
    try {
      const { data } = await axios.get("https://api.openbrewerydb.org/breweries");

      this.setState({ breweries: data });
    } catch (err) {
      console.error(err);
    }
  }

  //   componentDidMount() {
  //     axios.get("https://api.openbrewerydb.org/breweries")
  //       .then((response) => {
  //         const { data } = response;
  //         this.setState({ breweries: data });
  //       }).catch(error => console.error(err))
  //   }

  render() {
    return (
      <div>
        {this.state.breweries.map((brewery) => (
          <div key={brewery.id} className='brewery'>
            <p>{brewery.name}</p>
          </div>
        ))}
      </div>
    );
  }
}

export default BreweryList;
```
