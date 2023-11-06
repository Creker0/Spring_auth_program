## User Authorization and Authentication System

This repository contains a simple user authorization and authentication system implemented in Java using the Spring Framework, Spring Security, and PostgreSQL as the database. The system allows users to sign up, sign in, and generates JWT (JSON Web Tokens) for secure authentication.

### Features

- User signup: Users can create a new account with a unique username and email address.
- Password hashing: User passwords are securely hashed using the BCrypt password encoder.
- User signin: Registered users can sign in to get an authentication token.
- JWT authentication: The system uses JSON Web Tokens (JWT) for secure user authentication.
- CORS support: Cross-Origin Resource Sharing (CORS) is configured for flexible client integration.

### Technologies Used

- Spring Framework
- Spring Security
- Spring Data JPA
- PostgreSQL
- BCrypt Password Encoder
- JSON Web Tokens (JWT)

### Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/Creker0/Spring_auth_program
   cd Spring_auth_program
   ```

2. Configure the PostgreSQL database in `application.properties`.

3. Build and run the application using Gradle or your preferred IDE.

   ```bash
   ./gradlew bootRun
   ```

4. Access the API endpoints to sign up and sign in users.

### API Endpoints

- `POST /auth/signup`: Register a new user account by providing a username, email, and password.
- `POST /auth/signin`: Sign in with your username and password to receive a JWT token.

### Sample Requests

**Signup:**

```http
POST /auth/signup
Content-Type: application/json

{
  "username": "newuser",
  "email": "newuser@example.com",
  "password": "password123"
}
```

**Signin:**

```http
POST /auth/signin
Content-Type: application/json

{
  "username": "newuser",
  "password": "password123"
}
```

### Security

This project uses Spring Security for protecting the API endpoints and ensuring secure user authentication. The system securely hashes user passwords, and JWTs are used for authentication.

### Roadmap

- Implement email verification for user signup.
- Add user roles and authorization for different user access levels.
- Enhance error handling and validation.

### Contribute

Feel free to contribute to this project by opening issues, suggesting improvements, or creating pull requests. Your contributions are welcome!

Happy coding!
