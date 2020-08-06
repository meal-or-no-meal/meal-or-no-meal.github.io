## Meal or no Meal API

### Overview
The Meal or no Meal API is organized around REST and is designed to have predictable, resource-oriented URLs. The API supports requests and responses in JSON format.

## Queries
For each request when running backend server package locally send Query strings to: http://localhost:8080/.  There is no other or token authentication required. 


### HTTP Methods
The Meal or no Meal API uses standard HTTP methods as actions for all API requests. The table below is a general rule of thumb for which HTTP methods are used.

|Method |Description   |  
|-----|-----|
|GET   | Retrieves a single object or a list of objects   |
|POST   | 	Creates an object or a relationship between objects  |   
|PUT   | 	Updates an object.  |  
|DELETE   |  	Deletes an object. |  

## Endpoints

| Endpoint  | Description  | 
|---|---|
| GET /meals  |Returns all meals for user   |  
| GET /meals{id}  |Returns meal based on User Id   | 
| GET /ingredients/ | Returns all ingredients for a user | 
| GET /ingredients/{id} | Returns ingredient by Id | 
| GET /calendars/{id} | Returns all calendar items by Id |    
| POST /meals/ | Create a meal  |
| POST /calendars/ | Create a calendar item |
| PUT /meals/{id} | Update a meal  |  
| DELETE /meals/{id} | Deletes a meal  |  
| DELETE /calendar/{id} | Deletes a calendar item  |  
