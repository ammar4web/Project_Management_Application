<p align="center">
    <a href="https://laravel.com" target="_blank">
        <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
    </a>
</p>
<hr />

## Project Installation Steps:

1. Clone the repository:
2. Create the ".env" file and set the database connection values.
3. Install project dependencies:
4. Generate the application key:
5. Run database migrations:

<hr />

## API Routes

All routes are prefixed with `/api/v1/`.

### Authentication

- **Register User**
    * `POST /api/v1/auth/register`
    * Register a new user.
    * ```
    {
        "name": "John Doe",
        "email": "john@example.com",
        "password": "your_password_here",
        "password_confirmation": "your_password_here"
    }
        ```

- **User Login**
    * `POST /api/v1/auth/login`
    * Log in an existing user.
    * ```
    {
        "email": "john@example.com",
        "password": "your_password_here"
    }
        ```

- **User Logout**
    * `POST /api/v1/auth/logout`
    * Log out the authenticated user. Requires API token.

### Profile

- **View User Profile**
    * `GET /api/v1/profile`
    * Retrieve the profile data of the authenticated user. Requires API token.

- **Update User Profile**
    * `PUT /api/v1/profile`
    * Update the profile data of the authenticated user. Requires API token.
    * ```
    {
        "name": "Updated Name",
        "email": "updated@example.com"
    }
    ```

- **Update Password**
    * `PUT /api/v1/password`
    * Update the password of the authenticated user. Requires API token.
    * ```
    {
        "current_password": "your_current_password",
        "password": "your_new_password",
        "password_confirmation": "your_new_password"
    }
    ```
