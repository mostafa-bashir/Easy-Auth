# Easy-Auth
# Node.js Project with MySQL, EJS, JavaScript, and CSS

## Description
This project is a web application built using Node.js, MySQL, EJS, and JavaScript. The application provides a simple authentication system with features for user registration, login, and profile management.

### Key Features:
1. **User Signup and Login:**
   - Users can create an account by signing up with their name, email, password, and age.
   - Registered users can log in to access their profile and other main features.

2. **User Profile Management:**
   - Logged-in users can view and edit their profile information.
   - All changes are saved to the MySQL database.

3. **Session-Based Authentication:**
   - The application uses sessions to maintain user authentication.
   - Users who are already logged in are redirected to the main screen without needing to log in again.
   - Unauthorized access to the main screen is blocked, and users are redirected to the login page if not authenticated.

4. **Environment Variables:**
   - Sensitive configurations, such as database credentials, are stored securely using `.env` files.

5. **Password Hashing:**
   - User passwords are securely hashed before being stored in the database.

6. **CSS Design:**
   - The application includes a clean and responsive design using CSS for better user experience.

## Technologies Used
- **Node.js:** Backend runtime environment for building server-side logic.
- **MySQL:** Relational database for storing user information.
- **EJS:** Templating engine for rendering dynamic views.
- **JavaScript:** Frontend scripting for interactivity and validation.
- **CSS:** For designing a responsive and visually appealing user interface.
- **dotenv:** For managing environment variables.
- **bcrypt:** For hashing passwords securely.

## Installation

1. Clone the repository:
   ```bash
   git clone <https://github.com/mostafa-bashir/Easy-Auth.git>
   ```

2. Navigate to the project directory:
   ```bash
   cd <project-directory>
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Set up the MySQL database:
   - Create a database and import the provided SQL file (if available).
   - Create a `.env` file in the project root and add your database configuration:
     ```env
     DB_HOST=localhost
     DB_USER=your-username
     DB_PASSWORD=your-password
     DB_NAME=your-database-name
     ```

5. Start the server:
   ```bash
   npm start
   ```

6. Open your browser and navigate to:
   ```
   http://localhost:8000
   ```

## Application Structure
- **Routes:**
  - `/signup`: User registration page.
  - `/login`: User login page.
  - `/main`: Main screen for logged-in users (profile management).

- **Middleware:**
  - Session middleware ensures that only authenticated users can access the main screen.
  - Redirects unauthenticated users to the login page.

## Usage
1. **Sign Up:**
   - Navigate to the sign-up page.
   - Fill in your details and create an account.

2. **Log In:**
   - Log in using your registered email and password.

3. **Edit Profile:**
   - After logging in, update your profile details on the main screen.
   - Save changes to update the database.

4. **Session Handling:**
   - Close and reopen your browser. If you are still logged in, you will be redirected directly to the main screen.
   - If not logged in, any attempt to access `/main` will redirect you to the login page.

## Future Enhancements
- Add email verification during signup.
- Integrate additional features like forgot password and profile picture uploads.
- Further enhance the CSS design for a modern look and feel.

## License
This project is open-source and available under the [MIT License](LICENSE).

---

Feel free to contribute, report issues, or suggest improvements!

