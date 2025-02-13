During my 3rd Semester, I've learn about Object-Oriented Programming(OOP). All of the pillars of OOP have been applied in this project and also some addition about Application Programming Interface (API). So here we go :)

### Project Overview
- **Title**: Book Management API
- **Description**: A RESTful API for managing books, including CRUD operations, user authentication, and authorization. Built with ASP.NET Core, Entity Framework Core, and Identity for user management.

### Features
- **Book Management**:
  - **Get All Books**: Retrieve a list of all books.
  - **Get Book by ID**: Retrieve a specific book by its ID.
  - **Add Book**: Add a new book (Admin role required).
  - **Update Book**: Update an existing book (User role required).
  - **Delete Book**: Delete a book by its ID (Admin role required).
  - **Search Books**: Search books by title.

- **User Authentication and Authorization**:
  - **User Registration**: Register a new user.
  - **User Login**: Authenticate and generate a JWT token.
  - **Token Refresh**: Refresh an expired JWT token.

### Technologies Used
- **Backend**: ASP.NET Core
- **Database**: SQLite with Entity Framework Core
- **Authentication**: ASP.NET Core Identity with JWT (JSON Web Tokens)
- **Dependency Injection**: Built-in ASP.NET Core DI
- **AutoMapper**: For object-to-object mapping
- **Swagger**: API documentation and testing

### Setup and Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/TohPakAng98/asp-dotnet-web-api.git
   cd asp-dotnet-web-api
   ```

2. **Install Dependencies**:
   ```bash
   dotnet restore
   ```

3. **Database Setup**:
   - Ensure SQLite is installed.
   - Update the connection string in `appsettings.json`.
   - Run migrations to create the database:
     ```bash
     dotnet ef database update
     ```

4. **Run the Application**:
   ```bash
   dotnet run
   ```

5. **Access Swagger UI**:
   - Navigate to `https://localhost:5001/swagger` to explore the API endpoints.

### API Endpoints
- **Books**:
  - `GET /api/books`: Get all books.
  - `GET /api/books/{id}`: Get a book by ID.
  - `POST /api/books`: Add a new book.
  - `PUT /api/books/{id}`: Update a book.
  - `DELETE /api/books/{id}`: Delete a book.
  - `GET /api/books/search`: Search books by title.

- **Authentication**:
  - `POST /api/auth`: Register a new user.
  - `POST /api/login`: Authenticate and get a JWT token.
  - `POST /api/refresh`: Refresh an expired JWT token.

### Error Handling
- Custom exception handling middleware is implemented to return consistent error responses.
- Common HTTP status codes:
  - `200 OK`: Successful request.
  - `201 Created`: Resource created successfully.
  - `204 No Content`: Successful request with no content to return.
  - `400 Bad Request`: Invalid request data.
  - `401 Unauthorized`: Authentication required.
  - `404 Not Found`: Resource not found.
  - `422 Unprocessable Entity`: Validation errors.

### Security
- **Authentication**: JWT-based authentication.
- **Authorization**: Role-based access control (Admin, User).
- **CORS**: Configured to allow cross-origin requests.

### Contributing
- Contributions are welcome! Please fork the repository and submit a pull request.

### License
- This project is licensed under the MIT License. See the `LICENSE` file for details.

### Acknowledgments
- Thanks to the ASP.NET Core team for the excellent framework and tools.

