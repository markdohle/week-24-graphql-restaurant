# week-24-graphql-restaurant
MIT xPro - Week 24 GraphQL and CRUD

### Queries and Mutations used in GraphiQL Browser Tool

```
query restaurant($idd: Int = 2){
	restaurant(id:$idd) {
    name
  }
}

query restaurants { 
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Fudruckers",
    description: "Kids and all",
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

mutation editrestaurants($idd: Int = 1, $name: String = "New Name") {
  editrestaurant(id: $idd, name: $name) {
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
```
