# JSP E-Commerce Shopping Cart

A full-stack Java-based web application that simulates an online shopping experience using JSP, Servlets, JDBC, and MySQL. This project demonstrates a complete e-commerce workflow — from browsing products and adding items to a cart, to logging in, placing, and managing orders.

---

## Features

- Product browsing and detailed view
- User authentication and session management
- Shopping cart operations: add, update quantity, remove
- Order placement and cancellation
- Admin-oriented order view
- Clean modular MVC design (Servlets + JSP + DAO)

---

## Use Cases

- Browse Products: Users can view a product catalog with images, names, and prices.
- Add to Cart: Logged-in users can add selected products to their cart.
- Update Cart Quantity: Users can increase or decrease quantities in the cart.
- Remove from Cart: Users can remove items anytime before checkout.
- Place Order: Proceed to checkout and place an order.
- User Authentication: Secure login/logout functionality.
- View Orders: Users can review their order history and details.
- Cancel Order: Cancel unprocessed orders.

---

## Requirements

- Java JDK 8 or later
- Apache Tomcat 9 or 10
- MySQL Server (XAMPP, MAMP, etc.)
- IDE (VS Code, IntelliJ IDEA, or Eclipse)
- Maven (for build and dependency management)

---

## Setup Instructions

1. **Database Setup**

   - Create the database:
     ```sql
     CREATE DATABASE ecommerce;
     ```

   - Import the SQL schema:
     ```bash
     mysql -u root -p ecommerce < database/20210519.sql
     ```

2. **Configure Database Connection**

   - Edit the file: `src/cn/techtutorial/connection/DbCon.java`

   - Update with your MySQL credentials:
     ```java
     private static final String URL = "jdbc:mysql://localhost:3306/ecommerce";
     private static final String USER = "root";
     private static final String PASSWORD = ""; // your MySQL password
     ```

3. **Build and Deploy**

   - Compile and package the project:
     ```bash
     mvn clean package
     ```

   - Deploy to Tomcat:
     - Option 1: Copy the `.war` file from `/target` to `TOMCAT_HOME/webapps/`
     - Option 2: Copy the entire `jsp-ecommerce-master` folder to `webapps/`

   - Start Tomcat:
     ```bash
     ./startup.sh   # macOS/Linux
     startup.bat    # Windows
     ```

   - Open your browser and go to:
     ```
     http://localhost:8080/jsp-ecommerce-master
     ```

---

## Default Login Credentials

- Username: admin  
- Password: admin123  
*(Check the users table in your database if these have been changed.)*
