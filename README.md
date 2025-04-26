# apexplanet-webdeveloper-PHP-MYSQL-

# Task 1: User Authentication Setup

## Overview

This project implements a basic user authentication system as part of the Web Development Internship Program at ApexPlanet Software Pvt Ltd. The system includes user registration and login functionalities, built using PHP and MySQL.

## Features

* **User Registration:** Allows new users to create an account by providing their name, email, and password.
* **User Login:** Authenticates existing users and grants them access to the system.
* **Database Integration:** Stores user credentials securely in a MySQL database.
* **Password Hashing:** Protects user passwords by using the `password_hash()` function.
* **Session Management:** Manages user login sessions using PHP sessions.

## Technologies Used

* PHP
* MySQL
* HTML
* CSS
* JavaScript (for client-side validation)
* XAMPP/WAMP (for local development environment)

## Setup Instructions

1.  **Install XAMPP/WAMP:**
    
    * Download and install XAMPP or WAMP on your system.
2.  **Clone the Repository:**
    
    * Clone this GitHub repository to your local machine.
3.  **Create Database:**
    
    * Open phpMyAdmin (usually accessible at `http://localhost/phpmyadmin`).
    * Create a new database (e.g., `internship_db`).
    * Create a `users` table with the following structure:
        
        ```sql
        CREATE TABLE users (
            id INT AUTO_INCREMENT PRIMARY KEY,
            name VARCHAR(255) NOT NULL,
            email VARCHAR(255) NOT NULL UNIQUE,
            password VARCHAR(255) NOT NULL
        );
        ```
        
4.  **Configure Database Connection:**
    
    * Edit the `config.php` file (if you have one, or create one) to include your database connection details:
        
        ```php
        <?php
        $host = "localhost";
        $username = "root"; // Default username for XAMPP/WAMP
        $password = "";     // Default password for XAMPP/WAMP is often empty
        $database = "internship_db";
        
        $conn = mysqli_connect($host, $username, $password, $database);
        
        if (!$conn) {
            die("Connection failed: " . mysqli_connect_error());
        }
        ?>
        ```
        
5.  **Place Files in htdocs:**
    
    * Place the project files (e.g., `register.php`, `login.php`, etc.) in the `htdocs` folder (for XAMPP) or `www` folder (for WAMP).
6.  **Access the Application:**
    
    * Open your web browser and navigate to `http://localhost/your_project_folder/register.php` to access the registration page, or  `http://localhost/your_project_folder/login.php` to access the login page.

## Project Structure


├── config.php        # Database connection configuration
├── css/            # CSS stylesheets
│   └── style.css
├── js/             # JavaScript files
│   └── validation.js
├── register.php      # User registration page
├── login.php         # User login page
└── README.md       # Project documentation (this file)


##  Important Considerations

* **Security:** Password hashing is implemented using PHP's `password_hash()` function for security.
* **Validation:** Client-side validation (using JavaScript) and server-side validation (using PHP) are used to ensure data integrity.
* **Error Handling:** Error handling is implemented to provide user-friendly error messages.

##  Deliverables

* Functional user registration and login pages.
* Database setup and connection code.
* Secure password storage.
* Basic styling and responsive design.

##  Author

* Cheedella Venkata Sai Chetan Kumar

##  Contact

* Email: chetankumar12538@gmail.com
* Phone: +91 9494437501
  
