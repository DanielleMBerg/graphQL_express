# graphQL_express
Allows you to query a list of restauarants.

# Possible queries
mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}

# How to Run
To run on your own device, download all the files (except for the LICENSE file and the README file) and save them in one folder. Open your terminal, navigate to the folder with the files, install dependencies by writing 'npm install,' than start program with 'node index.js.' Access by navigating to localhost:5500//graphql in your browser.
