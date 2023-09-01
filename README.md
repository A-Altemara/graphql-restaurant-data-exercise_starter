# GraphQL Restruant Data Exercise

This is a practice exercise for handling data with API endpoints. Using a Database and GraphQL. It's designed to create a practice ground for testing the GraphQL queries and understanding out the UI for the GraphQL playground enables better visuals of a database. Queries that can be run are listed below.

## How to run

In the terminal type node index.js to start the server then navigate to localhost:5500/graphql

### Queries that can be run are as follows:

mutation editrestaurants($idd: Int!, $name: String!) {
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

mutation deleterestaurants($iid: Int!) {
deleterestaurant(id: $iid) {
ok
}
}

query getresturant ($iid:Int!){
  restaurant(id:$iid){
name
description
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

MIT License
Copyright (c) 2023 Airiel Altemara

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
