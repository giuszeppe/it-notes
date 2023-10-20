Here I want to explain some of the limitations of the REST approach, pointing out that following [[REST - best_practices]] the can be partially solved.

#### Flexibility
A **REST-API** is clearly constrained to HTTP Verbs and often his structure reflects the structure of a Database, and so it's clear that, other than exposing information to potential attacker, this leads to less flexibility because if the DB shape changes, the API must change accordingly.

#### Huge numbers of endpoint
REST will have, as the time goes on, lots of endpoints to discover and document.
 
#### Under-fetching
This happens when our response returns less data than we need, and so we do another requests to gather all the information we need.
-- TODO: Add Examples

#### Over-fetching
On the other hand, it could happen that our API returns more data than we need, and so we lose performance in exchange of useless data.


## Resources
https://www.imaginarycloud.com/blog/graphql-vs-rest/#Graph
https://www.thepowermba.com/en/blog/rest-api-what-it-is