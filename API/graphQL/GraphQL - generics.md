GraphQL is a **stateless**, **client-independent**, **strongly-typed** declarative query language for APIs and a server-side runtime for executing typed queries on your data.
#### What problem does it solve?
It enhances the flexibility of you API providing a rich query-language. To speak about the problems that GraphQL solves, we must understand the problems that [[REST - limitations]] has. 
With GraphQL, clients can requests only the data they need using the query language.
This ensures faster development, more flexibility and also better performances since no useless data is provided to the clients. 

#### How does it work?
It uses a single-endpoint in which you should provide a query as the body to define the data that should be returned.
Every GraphQL service defines a set of types that describe the possible data you can query on that service (that’s the **schema**). 
**queries and mutations** are validated and executed against that schema and processed using **resolvers**.

So a complete GraphQL implementation must have two parts: **schemas & resolvers**.
![[graphql_diagram.png]]
###### Operation Types
- **Query** (GET)
- **Mutation** (POST,PUT,PATCH,DELETE)
- **Subscription** (Real-time)
###### Entities
- **Schema** (set of tyes)
- **Resolvers** (who processes the data)

#### How does a query look like?
```json
{
	user {
		name,
		friends {
			age
		}
	}
}
```

## Resources
https://scandiweb.com/blog/what-is-graphql-api-how-does-it-work/
https://graphql.org/learn/