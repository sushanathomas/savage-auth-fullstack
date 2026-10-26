# 21 Savage Fan Site — With Authentication

A full-stack message board with signup and login using Passport.

I built this project to practice authentication, sessions, and CRUD functionality with Express and MongoDB.

## Live Application

<!-- Add the Render website link after deployment. -->

## Screenshot

<!-- Add a screenshot of the application here. -->

## Features

- Create an account, log in, and log out.
- Access the profile page while logged in.
- Add messages.
- View saved messages.
- Increase and decrease message votes.
- Delete messages.
- View an embedded GIF from GIPHY.

## Design

The application uses a blue background, white panels, and green buttons.

The login and profile pages use a font stack starting with Trebuchet MS, with fallback fonts for devices that do not have it installed.

## CRUD Functionality

- **Create:** Add a message.
- **Read:** Display saved messages.
- **Update:** Change a message’s vote count.
- **Delete:** Remove a message.

## Tools Used

- **Node.js:** Runs the server.
- **Express:** Handles requests and routes.
- **EJS:** Displays pages and database information.
- **MongoDB Atlas:** Hosts the database.
- **Mongoose:** Defines the user model and connects to MongoDB.
- **MongoDB Node.js driver:** Supports database operations and document IDs.
- **Passport and passport-local:** Handle email-and-password authentication.
- **bcrypt-nodejs:** Hashes passwords and checks them during login.
- **express-session:** Maintains login sessions.
- **connect-flash:** Displays signup and login messages.
- **dotenv:** Loads private environment settings.
- **JavaScript:** Handles voting and delete requests.
- **CSS and Bootstrap:** Style the pages and responsive layout.
- **Nodemon:** Restarts the server during development.

## How It Works

When someone signs up, the application hashes their password before saving the account.

Passport checks login details and uses a session to remember the logged-in user. The profile route checks whether the user is authenticated before displaying the page.

Express handles message requests, MongoDB stores the data, and EJS displays the saved information. Browser JavaScript sends requests when voting or deleting messages.

## Run Locally

1. Clone this repository and open its folder.

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the project root:

   ```env
   MONGODB_URI=your_mongodb_connection_string
   MONGODB_DB_NAME=savage-auth
   SESSION_SECRET=your_private_session_secret
   ```

4. Use your own Atlas credentials and allow your current IP address in Atlas.

5. Start the server:

   ```bash
   npm start
   ```

6. Open [http://localhost:8080](http://localhost:8080).

Keep `.env` and `node_modules/` out of Git using `.gitignore`.

## Main Files

- `server.js` — Sets up Express, MongoDB, Passport, and sessions.
- `config/database.js` — Loads database settings.
- `config/passport.js` — Defines authentication strategies and session handling.
- `app/models/user.js` — Defines user information and password methods.
- `app/routes.js` — Handles page, authentication, and message routes.
- `views/` — Contains the EJS templates.
- `public/main.js` — Handles message button interactions.
- `public/style.css` — Contains the custom styling.

## What I Learned

- How signup and login work with Passport.
- How password hashing differs from displaying a password.
- How sessions maintain a login.
- How to protect a page with authentication middleware.
- How to build CRUD features with Express and MongoDB.
- How to use environment variables for private settings.
- How to style pages and embed media.

## Credits

- Adapted from the `savage-auth` starter provided through Resilient Coders coursework.
- GIF/sticker hosted on [GIPHY](https://giphy.com/).
- [View the Pharrell Williams “Cash In Cash Out” sticker on GIPHY](https://giphy.com/stickers/pharrell-transparent-pharrell-williams-cash-in-out-oQ0gHOSOEIamfErIZO).

I do not claim ownership of the GIF/sticker or its underlying imagery.