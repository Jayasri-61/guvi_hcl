# PHP Login & Registration System

[![PHP](https://img.shields.io/badge/PHP-%3E%3D7.0-blue)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-%3E%3D5.7-green)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

A **secure, simple, and modular PHP login & registration system** using MySQL and PDO, designed for easy deployment on free or paid PHP hosting platforms like **InfinityFree**.

---

## 📂 Project Structure

```
.
├── css/
│   └── style.css           # Styles for login, register, profile pages
├── js/
│   ├── login.js            # Login form client-side logic
│   ├── profile.js          # Profile page client-side logic
│   └── register.js         # Registration form client-side logic
├── php/
│   ├── db.php              # Database connection using PDO
│   ├── login.php           # Handles login requests
│   ├── profile.php         # Fetches and displays user profile data
│   └── register.php        # Handles user registration requests
├── login.html              # Login page
├── profile.html            # Profile page
├── register.html           # Registration page
└── README.md               # Project documentation
```

---

## ⚙️ Features

* ✅ **User registration** with email, password, and optional profile details
* ✅ **Secure password storage** using `password_hash()` (Bcrypt)
* ✅ **User login** with `password_verify()`
* ✅ Automatic **password rehashing** if cost factor or algorithm changes
* ✅ **Profile management** for viewing user information
* ✅ **Prepared statements** to prevent SQL injection

---

## 🛠 Installation & Setup

1. **Clone the repository**

```bash
git clone https://github.com/Jayasri-61/guvi_hcl/new/main/projects
```

2. **Upload files** to your hosting server

   * For InfinityFree, place all files in the `htdocs/` directory.

3. **Create a MySQL database**

   * Access phpMyAdmin and create a new database.
   * Run the SQL script to create the `users` table:

```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    fullname VARCHAR(100) NOT NULL,
    email VARCHAR(150) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    age INT NULL,
    dob DATE NULL,
    contact VARCHAR(20) NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

4. **Configure database connection**

   * Edit `php/db.php` with your database credentials:

```php
define('DB_HOST','your_host');
define('DB_USER','your_user');
define('DB_PASS','your_password');
define('DB_NAME','your_database');
```

5. **Test your site**

   * Visit `login.html` or `register.html` in your browser.

---

## 🔒 Security

* Passwords are **hashed securely using Bcrypt**
* Uses **PDO with prepared statements** to prevent SQL injection
* Automatic **password rehashing** ensures updated security standards

---

## 💻 Tech Stack

* **Frontend:** HTML, CSS, JavaScript
* **Backend:** PHP (PDO)
* **Database:** MySQL

---

## 📌 Notes

* Fully compatible with **free PHP hosting like InfinityFree**
* Designed to be modular — easy to extend and customize

---

## 📄 License

MIT License – free to use, modify, and distribute
