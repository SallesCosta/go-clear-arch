# Clean Architecture Project in Go

<img src="./icons/go.svg" alt="go icon" width="60" height="60"> <img src="./icons/sw.svg" alt="swaggo icon" width="60" height="60"> <img src="./icons/gql.svg" alt="graphql icon" width="60" height="60"> <img src="./icons/grpc.svg" alt="grpc icon" width="60" height="60"> <img src="./icons/rabbitmq.svg" alt="rabbitmq icon" width="60" height="60"> <img src="./icons/mysql.svg" alt="mysql icon" width="60" height="60"> <img src="./icons/docker.svg" alt="docker icon" width="60" height="60">

## Clean Architecture

This project follows the principles of Clean Architecture, as proposed by Robert C. Martin. The main goal of this architecture is to make the system easy to understand, develop, test, and maintain.

The project is divided into four layers:

- **Entities**: These are the business objects of the application.
- **Use Cases**: This layer contains all the business rules of the application. It's independent of the UI, database, or any external agency.
- **Interface Adapters**: This layer is a set of adapters that convert data from the format most convenient for the use cases and entities, to the format most convenient for things like the web, database, and so on.
- **Frameworks and Drivers**: This is the outermost layer of the application and includes things like the web server and database management.

Each layer is isolated from the details of its adjacent outer layer. This means that the inner layers (Entities, Use Cases) are completely independent and the outer layers (Interface Adapters, Frameworks and Drivers) are dependent on them. This allows us to isolate and test business rules without the UI, Database, Web Server, or any other external element.

The communication between layers is done using interfaces and dependency rules, where the outer layers can depend on the inner layers, but not the other way around. This ensures that high-level modules are not dependent on low-level modules, making the system more flexible, easier to maintain, and less prone to bugs.
## Technologies Used 

- **Go**: The programming language used to develop the project.
- **REST**: One of the communication interfaces of the web server.
- **GraphQL**: Another communication interface of the web server, which allows for more efficient and flexible queries.
- **gRPC**: A high-performance communication interface of the web server.
- **Swaggo**: An automatic documentation tool for Go APIs.
- **SQLite3**: The database used for testing.
- **RabbitMQ**: Used for asynchronous communication between different parts of the system.
- **GoLand 2024.1.4**: The IDE used to develop the project.
- **Gqlgen**: A Go library for building GraphQL servers.
- **Chi**: A Go package for creating web routers.
- **Testify**: A Go library to facilitate writing unit tests.
- **Docker**: Used to containerize the application and its dependencies for consistent execution across different environments.```
 
## Running Unit Tests

The unit tests are located in `_test.go` files throughout the project. To run all unit tests, you can use the command `go test ./...` at the root of the project.

## Documentation

The documentation for the REST APIs is automatically generated using Swaggo. You can access the documentation by navigating to the `/swagger/index.html` endpoint on your local server after starting the project.

## Starting the Project

To start the project, you need to have Go installed on your system. After cloning the repository, you can start the server by running the command `go run cmd/ordersystem/main.go` at the root of the project.

This will start the web server on the port specified in the configuration file. You can then access the REST, GraphQL, and gRPC APIs at their respective endpoints.

## Contributing

Contributions are welcome! Please read the contribution guidelines before submitting a pull request.

## License

This project is licensed under the MIT license. See the `LICENSE` file for more details.
