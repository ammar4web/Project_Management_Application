<h2>API Routes</h2>

Here are the API routes for the application. All routes are prefixed with `/api/v1/`.

### Authentication Routes

- **Register User**
  - Endpoint: `POST /api/v1/auth/register`
  - Description: Register a new user.
  - Request Body:
    ```
    {
        "name": "John Doe",
        "email": "john@example.com",
        "password": "your_password_here",
        "password_confirmation": "your_password_here"
    }
    ```
  - Response: Returns the newly registered user data.

- **User Login**
  - Endpoint: `POST /api/v1/auth/login`
  - Description: Log in an existing user.
  - Request Body:
    ```
    {
        "email": "john@example.com",
        "password": "your_password_here"
    }
    ```
  - Response: Returns the authenticated user data and generates a new API token (Sanctum token).

- **User Logout**
  - Endpoint: `POST /api/v1/auth/logout`
  - Description: Log out the authenticated user.
  - Authentication: Requires an API token (Sanctum token) obtained during login.
  - Response: Returns no data (HTTP 204 No Content).

### Profile Routes

- **View User Profile**
  - Endpoint: `GET /api/v1/profile`
  - Description: Retrieve the profile data of the authenticated user.
  - Authentication: Requires an API token (Sanctum token).
  - Response: Returns the user's profile data.

- **Update User Profile**
  - Endpoint: `PUT /api/v1/profile`
  - Description: Update the profile data of the authenticated user.
  - Authentication: Requires an API token (Sanctum token).
  - Request Body:
    ```
    {
        "name": "Updated Name",s
        "email": "updated@example.com"
    }
    ```
  - Response: Returns the updated user profile data.

- **Update Password**
  - Endpoint: `PUT /api/v1/password`
  - Description: Update the password of the authenticated user.
  - Authentication: Requires an API token (Sanctum token).
  - Request Body:
    ```
    {
        "current_password": "your_current_password",
        "password": "your_new_password",
        "password_confirmation": "your_new_password"
    }
    ```
  - Response: Returns a success message upon successful password update.
