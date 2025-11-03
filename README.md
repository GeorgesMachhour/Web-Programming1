# Web-Programming1
Instrumentity - Online Musical Instruments Shop
Project Description
This project is a full-stack web application for an online musical instruments store named Instrumentity. The application allows users to browse a catalog of instruments, register accounts, add items to a shopping cart, and complete purchases. Administrators have access to a dedicated interface to perform full CRUD (Create, Read, Update, Delete) operations on the product inventory.

The backend is built with Node.js and Express, utilizing a MySQL database for data persistence. The frontend is dynamically rendered using EJS templates, providing a seamless and interactive user experience. The project follows modern web development practices, including a RESTful API structure and modular code organization.

Key Features
User Authentication: Separate login flows for administrators and regular customers.

Product Catalog: Dynamic listing of featured and all products.

Shopping Cart & Checkout: Users can add products to their cart and complete orders.

Admin Panel: Authorized users can create, view, update, and delete products.

RESTful API: A dedicated API for managing product data.

File Upload: Admins can upload product images (JPG) using Multer middleware.

Technology Stack
Backend: Node.js, Express.js

Database: MySQL

Frontend: EJS (Embedded JavaScript templating), CSS

Other Dependencies:

body-parser - For parsing request bodies

mysql - MySQL client for Node.js

multer - Middleware for handling file uploads

async - For managing asynchronous operations

Project Structure
text
project-root/
│
├── DataBase/
│   └── connection.js          # Database configuration and connection
├── node_modules/              # Project dependencies (auto-generated)
├── routes/                    # Application route handlers
│   ├── account.js
│   ├── cart.js
│   ├── checkout.js
│   ├── dashboard.js
│   ├── index.js
│   └── products.js
├── shopweb/                   # Static assets (images, CSS, HTML)
├── SQL_Tables/                # SQL scripts for database schema
├── views/                     # EJS templates for dynamic pages
└── server.js                  # Main application entry point
Installation & Setup
Prerequisites:

Ensure Node.js and npm are installed on your machine.

Have a MySQL server running (e.g., via Laragon, XAMPP).

Clone the repository and install dependencies:

bash
npm install
Database Setup:

Create a MySQL database named instrumentify.

Run the SQL scripts located in the SQL_Tables/ directory to create the necessary tables (users, items, cart, checkout).

Configuration:

Update the database connection details in DataBase/connection.js with your own MySQL credentials (username, password, host).

Run the Application:

bash
node server.js
The application will be available at http://localhost:4500.

API Endpoints
The application provides a RESTful API for product management:

Method	Endpoint	Description
GET	/api/products	Retrieves all products.
GET	/api/products/:id	Fetches a single product by ID.
POST	/api/products	Adds a new product.
PUT	/api/products/:id	Updates an existing product by ID.
DELETE	/api/products/:id	Deletes a product by ID.
Default Admin Account
A default administrator account is pre-configured for testing:

Username: admin

Email: admin@admin.com

Password: admin123

Developer: Georges Machhour - 202110271
