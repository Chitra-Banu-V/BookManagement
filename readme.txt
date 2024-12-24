Project Overview :
The Book Management System API is a backend API built using ASP.NET Core. It manages book-related data, such as adding, updating, deleting books, and fetching book information. It serves as the backend for the Book Management System UI (front-end), providing data through HTTP API endpoints.

Key Features:

1. Add, update, and delete books.
2. Implement in 3 tire architecture(Controller, Service, Repository).
3. Validate the Inputs using FluentValidator.
4. Used AutoMapper mapping profile for object conversion.
5. Unit Test case using XUnit.

Project Structure :

The project follows a clean architecture with separate layers for Controllers, Services, and Repositories. Here's the directory structure:

BookManagementSystem.API/
│
├── Controllers/                # Contains API controllers for handling HTTP requests.
│   ├── BooksController.cs      # Manages routes for books (Add, Update, Delete, etc.).
│
├── Models/                     # Contains models (e.g., Book)
│   ├── Book.cs                 # Represents the Book entity.
├── DTOs/                     # Contains DTOs (e.g., BookDTO)
│   ├── BookDTO.cs                 # Represents the Book DTO.
├── DomainModels/                     # Contains domain models (e.g., BookModel)
│   ├── BookModel.cs                 # Represents the Book Model.
│
├── Services/                   # Business logic for handling book-related operations.
│   ├── BookService.cs          # Contains methods for business logic related to books.
│
├── Repositories/               # Handles data access and interaction with the database.
│   ├── BookRepository.cs       # Contains CRUD operations for the Book entity.
│
├── Migrations/                 # Contains database migration files.
├── Interfaces/                 # Contains interfaces for service and repository.
├── Validators/                 # Contains Fluentvalidator for input validation.
├── Tests/                      # Contains service layer test file.
│
├── BookManagementSystemContext.cs   # Contains Dbcontext.
├── mappingProfile.cs           # contains automapper mapping profile.
├── appsettings.json            # Configuration settings (e.g., database connection strings).
├── Program.cs                  # Entry point for the application, configures services.
└── Startup.cs                  # Configures middleware and routing (optional in .NET 6 and above).

Steps to Run the API:

Follow these steps to set up and run the Book Management System API locally:

1. Extract the ZIP file
Extract the contents of the ZIP file to a directory on your local machine.

2. Set Up Database
The API uses Entity Framework Core for data access. You'll need to configure the connection to your database and apply migrations to create the database schema.

a. Apply Migrations
To set up the database schema, open a terminal/command prompt, navigate to the BookManagementSystem.API folder, and run the following commands:

# Apply database migrations
       dotnet ef database update

This will create the database and the necessary tables for the application.

3. Run the API
       To start the API server, run the following command:
       dotnet run


