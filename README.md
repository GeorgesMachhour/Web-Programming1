```markdown
# 🎵 Instrumentity - Online Musical Instruments Shop

A full-stack web application for an online musical instruments store built with Node.js and MySQL.

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-8A2BE2?style=for-the-badge&logo=javascript&logoColor=white)

## 🚀 Features

### 👥 User Features
- **User Registration & Authentication** - Separate login flows for customers and admins
- **Product Catalog** - Browse featured and all products with images and details
- **Shopping Cart** - Add/remove items with quantity selection
- **Checkout System** - Complete purchase workflow
- **Responsive Design** - Clean and user-friendly interface

### 🛠️ Admin Features
- **Admin Dashboard** - Special access for product management
- **CRUD Operations** - Create, Read, Update, Delete products
- **Image Upload** - Upload product images (JPG format)
- **Inventory Management** - Manage product quantities and pricing

## 🛠️ Tech Stack

**Backend:**
- Node.js
- Express.js
- MySQL Database

**Frontend:**
- EJS Templating Engine
- CSS3
- JavaScript

**Key Dependencies:**
- `express` - Web application framework
- `mysql` - MySQL database client
- `body-parser` - Request body parsing
- `multer` - File upload handling
- `ejs` - Template engine
- `async` - Asynchronous control flow

## 📁 Project Structure

```
instrumentity/
├── DataBase/
│   └── connection.js          # Database configuration
├── routes/                    # Express route handlers
│   ├── account.js            # Authentication routes
│   ├── cart.js               # Shopping cart routes
│   ├── checkout.js           # Checkout process routes
│   ├── dashboard.js          # Admin dashboard routes
│   ├── index.js              # Main page routes
│   └── products.js           # Product management routes
├── shopweb/                   # Static assets
│   ├── images/               # Product images
│   ├── css/                  # Stylesheets
│   └── *.html                # Static HTML files
├── SQL_Tables/               # Database schema scripts
├── views/                    # EJS templates
└── server.js                 # Application entry point
```

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MySQL Server
- npm

### Step-by-Step Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/instrumentity.git
   cd instrumentity
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Database Setup**
   ```sql
   -- Create database
   CREATE DATABASE instrumentify;
   
   -- Or run the SQL scripts from SQL_Tables directory
   mysql -u your_username -p instrumentify < SQL_Tables/your_schema_file.sql
   ```

4. **Configure Environment**
   ```javascript
   // Update DataBase/connection.js with your credentials
   {
     host: 'localhost',
     user: 'your_mysql_username', 
     password: 'your_mysql_password',
     database: 'instrumentify'
   }
   ```

5. **Start the Application**
   ```bash
   node server.js
   ```

6. **Access the Application**
   Open your browser and navigate to: `http://localhost:4500`

## 🔌 API Endpoints

| Method | Endpoint | Description | Body |
|--------|-----------|-------------|-------|
| GET | `/api/products` | Get all products | - |
| GET | `/api/products/:id` | Get product by ID | - |
| POST | `/api/products` | Create new product | `{code, description, price, quantity}` |
| PUT | `/api/products/:id` | Update product by ID | `{code, description, price, quantity}` |
| DELETE | `/api/products/:id` | Delete product by ID | - |

## 👨‍💼 Default Accounts

**Admin Account:**
- **Username:** `admin`
- **Email:** `admin@admin.com` 
- **Password:** `admin123`

**Sample User Account:**
- **Username:** `georges777`
- **Email:** `georges@mail.com`
- **Password:** `pass777`

## 🗃️ Database Schema

### Tables Structure
- `users` - User accounts and authentication
- `items` - Product inventory and details  
- `cart` - Shopping cart items
- `checkout` - Order history and transactions

### Sample Data
```sql
mysql> SELECT * FROM users;
+----+-------------+-------------------+-----------+
| ID | Username    | email             | Password  |
+----+-------------+-------------------+-----------+
| 1  | admin       | admin@admin.com   | admin123  |
| 8  | georges777  | georges@mail.com  | pass777   |
+----+-------------+-------------------+-----------+
```

## 🎯 Usage Guide

### For Customers:
1. Register a new account or login
2. Browse products in the catalog
3. Add items to cart with desired quantities
4. Proceed to checkout to complete purchase

### For Administrators:
1. Login with admin credentials
2. Click on the cart icon in navbar to access admin dashboard
3. Use the admin panel to:
   - Add new products with images
   - Edit existing product details
   - Update inventory quantities
   - Remove products from catalog

## 🚀 Future Enhancements

- [ ] User authentication & authorization middleware
- [ ] Payment gateway integration (Stripe/PayPal)
- [ ] Advanced product search & filtering
- [ ] Order tracking system
- [ ] Product reviews & ratings system
- [ ] Wishlist functionality
- [ ] Email notifications
- [ ] Inventory alerts
- [ ] Sales analytics dashboard

## 🐛 Troubleshooting

**Common Issues:**
- **Port already in use**: Change port in `server.js`
- **Database connection failed**: Verify MySQL credentials in `connection.js`
- **File upload errors**: Ensure `shopweb/` directory has write permissions

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.


---

**Instrumentity: Your marketplace for the finest musical instruments!** 🎸🎹🥁

> *Where you'll find the latest music gear, and the best quality instruments.*
```

