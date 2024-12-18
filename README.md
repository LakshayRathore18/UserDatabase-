# User Database System

A simple user management system built with **Node.js**, **Express**, **MySQL**, and **EJS**. Users can:

- Join the platform by creating an account.
- View the list of all registered users.
- Search for specific users.
- Edit user information (with password verification).
- Delete users (with password verification).

## Features

1. **User Management**: Create, read, update, and delete users.
2. **Search Functionality**: Search users by username.
3. **Secure Actions**: Ensure critical operations like editing and deleting require password verification.
4. **Dynamic Views**: Responsive and styled user interface using EJS templates.

## Technologies Used

- **Node.js**: Backend runtime.
- **Express**: Web framework for Node.js.
- **MySQL**: Relational database for user data.
- **EJS**: Templating engine for rendering dynamic HTML.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/user-database-system.git
   cd user-database-system
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the MySQL database:
   - Create a database named `UserProject`.
   - Run the following SQL command to create the `user` table:
     ```sql
     CREATE TABLE user (
         id VARCHAR(255) PRIMARY KEY,
         username VARCHAR(255) NOT NULL,
         email VARCHAR(255) NOT NULL,
         password VARCHAR(255) NOT NULL
     );
     ```

4. Create a `.env` file to store your database credentials:
   ```env
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=Mys@95825
   DB_NAME=UserProject
   ```

5. Start the server:
   ```bash
   node index.js
   ```

6. Open your browser and navigate to `http://localhost:8080`.

## Folder Structure

```
user-database-system/
├── views/          # EJS templates
│   ├── home.ejs    # Home page
│   └── ...         # Other views
├── public/         # CSS/JS assets (optional)
├── index.js        # Main server file
├── README.md       # Project documentation
├── .gitignore      # Ignore unnecessary files
├── package.json    # Node.js dependencies
└── .env            # Environment variables (not included in repo)
```

## Usage

- **Homepage**: Displays the total number of users and options to join or view the user list.
- **User List**: Displays all users with options to edit or delete each user.
- **Search**: Search for users by their username.
- **Edit**: Update a user's username by providing their password.
- **Delete**: Remove a user from the database by confirming their password.

## Future Enhancements

- Add user authentication using sessions or JWT.
- Implement password hashing for better security.
- Enhance UI with modern CSS frameworks like Bootstrap or Tailwind.
- Add pagination for large user lists.
- Implement user roles and permissions.

## License

This project is open-source and available under the [MIT License](LICENSE).
