# REST API BEST PRACTICES
Here is a collection of practices that helped me designing my rest APIs
## Tips
Here are some tips gathered from videos, experience, etc (i'll quote the video when there is one)

### Where to generate the ID of a resource?
Generating ID in the API level is a good idea, but you have to be aware that if the IDs you're generating are auto-increment IDs, then you cannot story resource asyncronally since it could be a problem if the same ID is being created. The same problem exists if you're using a distributed environment (merging would lead to duplicate IDs problem). So, if you're working in a software that needs to scale / go distributed, be sure to use UUID and provide them at the API level.
### Use meaningful identifiers
While generating UUID, take in mind to use something human-understandable, not some useless identifier such as extreme-euclide-day-absurd
### Return the available actions along with the response
For example, if you have an order in which a user can call the cancel method, just return it a part of the response. This can help you when you're providing more functionalities, other than reducing the responsabilities of the frontend about the data.
```json
order : {
    ...
    actions : [ 
        {
            name: "CancelOrder",
            uri : "...",
            method: "PUT"
        }
    ]

}
```
### Prefer returning objects rather than plaintext
Objects provide you more freedom and more chance to update your response with zero-effort

### Never change the API
If you really need to do update (as usually happens) then you should use **API Versioning**. This can be achieved in 4 ways
**1. URI**
**2. Query Params**
**3. Headers**
**4. Media Type**

### Always catch exceptions and return meaningful errors

### Naming
ALWAYS use pluralized nouns
Use hypens instead of underscore

### Filtering, Sorting, Pagination
Be sure to add the possibility to restrict the fields that are returned
Be sure to add the possibility to limit the number of rows
Be sure to add the possibility to start the rows after x to allow pagination
**SORTING**
When sorting, be sure to add a _+_ or _-_ before the field to say ascendent or descendent 
`?sort=+name,-age`

### Idenmpotency 
Same request -> same response
No side effects
HTTP status can be differet 

### Async operations
When returning for an async request, be sure to return a `202 status code` and the location of an URL to check for the status of the operation

### Partial response
--- to be done --- 