# Pizza Tracker API

This is a Rails API for tracking pizza restaurants. It allows you to manage restaurants, pizzas, and their relationships.

### Getting Started

To get started with the application, follow these steps:

1. Clone this repository to your local machine.
2. Install Ruby and Rails if you haven't already.
3. Run bundle install to install the required gems.
4. Run rails db:migrate to run the database migrations.
5. (Optional) Run rails db:seed to populate the database with seed data.
6. Start the Rails server by running rails server.

The API will now be accessible at http://localhost:3000.

## API Endpoints

The following endpoints are available in the API:

### Restaurants

- GET /restaurants
Returns a list of all restaurants.

- GET /restaurants/:id
Returns detailed information about a specific restaurant and its associated pizzas.

- DELETE /restaurants/:id
Deletes a restaurant and all its associated pizzas.

### Pizzas

- GET /pizzas
Returns a list of all pizzas.

- POST /restaurant_pizzas
Creates a new restaurant-pizza association.

For detailed information about the expected request and response formats for each endpoint, refer to the Routes section below.

### Models and Associations

The following models are used in the application:

- Restaurant: Represents a pizza restaurant.
- Pizza: Represents a type of pizza.
- RestaurantPizza: Represents the association between a restaurant and a pizza.
The associations between the models are as follows:

- A Restaurant has many Pizzas through RestaurantPizza.
- A Pizza has many Restaurants through RestaurantPizza.
- A RestaurantPizza belongs to a Restaurant and belongs to a Pizza.

### Validations

The RestaurantPizza model has the following validation:

- price: Must be between 1 and 30.


### Routes

The API endpoints are mapped to the following routes:

- GET /restaurants
- GET /restaurants/:id
- DELETE /restaurants/:id
- GET /pizzas
- POST /restaurant_pizzas

For each route, the API returns JSON data in the specified format along with the appropriate HTTP status code.

Refer to the Requirements section for detailed examples of the expected request and response formats.

### Testing

To test the API endpoints, you can use tools like cURL, Postman, or testing frameworks like RSpec or MiniTest.

Refer to the Testing section in the README for detailed instructions on how to test the API and ensure its functionality.

## Author

Dennis Mutuma Marangu.


## License

This project is licensed under the MIT License.
