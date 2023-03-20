##Objective:
Create a Rails API backend for a pizza restaurant tracking app with at least three resources (three database tables) and implement associations.

##Models:
Create the following relationships:

A Restaurant has many Pizzas through RestaurantPizza
A Pizza has many Restaurants through RestaurantPizza
A RestaurantPizza belongs to a Restaurant and belongs to a Pizza
##Routes:
Implement the following routes:

GET /restaurants: Return a JSON array of all restaurants with their id, name, and address.
GET /restaurants/:id: Return a JSON object of a specific restaurant by id with its name, address, and a nested array of its pizzas with their id, name, and ingredients. If the restaurant is not found, return an error message with the appropriate HTTP status code.
DELETE /restaurants/:id: Remove a specific restaurant by id from the database along with any associated RestaurantPizzas. If the restaurant is not found, return an error message with the appropriate HTTP status code.
GET /pizzas: Return a JSON array of all pizzas with their id, name, and ingredients.
POST /restaurant_pizzas: Create a new RestaurantPizza that is associated with an existing Pizza and Restaurant. Accept an object with price, pizza_id, and restaurant_id in the body of the request. If the RestaurantPizza is created successfully, return a JSON object of the associated Pizza with its id, name, and ingredients. If not, return an error message with the appropriate HTTP status code.
##Validations:
Add a validation to the RestaurantPizza model that requires the price to be between 1 and 30.



