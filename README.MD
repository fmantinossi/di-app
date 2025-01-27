# Dependency Injection Study Project

This Go application was created as a study project to explore the concept of Dependency Injection using [Google Wire](https://github.com/google/wire). The project utilizes SQLite3 as an example of database dependency injection.

## Features

- **Dependency Injection**:
  - The project demonstrates how to use Google Wire to manage dependencies in a clean and maintainable way.

- **SQLite3 Database**:
  - SQLite3 is used as a lightweight database to exemplify how database dependencies can be injected into various components.

## Project Structure

```
DI-APP
├── product
│   ├── entity.go          # Defines the data models
│   ├── repository.go      # Handles database operations
│   └── usecase.go         # Contains business logic
├── .gitignore             # Git ignore file
├── go.mod                 # Go module file
├── go.sum                 # Dependencies checksum
├── LICENSE                # License file
├── main.go                # Entry point of the application
├── README.md              # Project documentation
├── wire.go                # Wire setup for dependency injection
└── wire_gen.go            # Generated code by Google Wire
```

## Getting Started

### Prerequisites

- Go 1.20+
- Google Wire installed ([Installation Guide](https://github.com/google/wire))

### Running the Application

1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd DI-APP
   ```

2. **Generate Wire Code**:
   - Use Google Wire to generate the dependency injection code:
     ```bash
     wire
     ```

3. **Run the Application**:
   - Execute the following command to run the project:
     ```bash
     go run main.go wire_gen.go
     ```

## Notes

- The `product` package contains the core business logic, separated into entities, repositories, and use cases.
- The `wire.go` file is used to define how dependencies are wired together, and `wire_gen.go` is the generated file that contains the actual implementation.
- SQLite3 is included only for demonstration purposes and should be replaced with a production-grade database in real-world applications.

## License

This project is for educational purposes and is licensed under the [MIT License](LICENSE).