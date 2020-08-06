## Meal or no Meal API

### Overview
The Meal or no Meal API is organized around REST and is designed to have predictable, resource-oriented URLs. The API supports requests and responses in JSON format.

### Queries
For each request when running backend server package locally send Query strings to: http://localhost:8080/.  There is no token or other authentication required. 


### HTTP Methods 
The Meal or no Meal API uses standard HTTP methods as actions for all API requests. The table below is a general rule of thumb for which HTTP methods are used.

|Method |Description   |  
|-----|-----|
|GET   | Retrieves a single object or a list of objects   |
|POST   | 	Creates an object or a relationship between objects  |   
|PUT   | 	Updates an object.  |  
|DELETE   |  	Deletes an object. |  

### Endpoints
| Endpoint  |  Description  |Authentication Required | Path Variables  | Request Body | Request Parmas  | Request Header | Return type |
|---|---|---|---|---|---|---|---|
| GET /meal{id} | Returns meal based on Meal Id | Yes |  | Long id |  |  | Meal | 
| GET /meals  | Returns all meals in repository and orders by name | Yes |  |  | |  | Iterable\<Meal\> | 
| GET /search | Returns all meals with names containing search parameter | Yes |  |  | (name = "q")String filter |  |  | 
| GET /search | Returns all calendar items by date range | Yes |   |   | (params = "from", "to") searchByDate | | Iterable\<Calendar\> | 
| GET /ingredients/ | Returns all ingredients for a user | Yes |  |   |   |  | Iterable\<Ingredients\> | 
| GET /ingredient/{id} | Returns ingredient by Id | Yes |  |   |  |  | Ingredient | 
| GET /calendar/{id} | Returns all calendar items by Id | Yes |  |   |  |  | Calendar | 
| GET /list_items/{id} | Returns all ingredients items by Id | Yes |  |   |  |  |  | 
| POST /meal/ | Creates a meal  | Yes |  | Meal meal |  |  | ResponseEntity\<Meal\> | 
| POST /calendar/ | Create a calendar item | Yes |  | Calendar calendar |  |  | ResponseEntity\<Calendar\> | 
| POST /ingredient/ | Creates an ingredient  | Yes |  | Ingredient ingredient |  |  | ResponseEntity\<Ingredient\> | 
| PUT /meal/{id}/meal-name | Update a meal name | Yes | Long id | String name |  |  | Meal | 
| PUT /meal/{id}/instruction | Update a meal recipe | Yes | Long id | String recipe |  |  | Meal |
| PUT /meal/{id}/prep | Update a meal prep time | Yes | Long id | int prepTime |  |  | Meal |
| PUT /meal/{id}/requirements | Update a meal tool requirements | Yes | Long id | String requirements |  |  | Meal | 
| PUT /meal/{id}/ingredients/{ingredientId} | Update a meal ingredients | Yes | Long id, long ingredientId | Ingredient ingredient | | | Ingredient | 
| DELETE /meals/{id} | Deletes a meal  | Yes |  |  |  |  | void | 
| DELETE /calendar/{id} | Deletes a calendar item  | Yes |   |  |  |  |  void | 
| DELETE /ingredient/{id} | Deletes an ingredient item  | Yes | Long id, long ingredientId |   |  |   |  void | 
