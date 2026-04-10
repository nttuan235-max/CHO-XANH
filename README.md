# 🛒 Chợ Xanh Market

A full-featured e-commerce web application built with PHP following the MVC architecture. Chợ Xanh allows customers to browse products, manage a shopping cart, and place orders — while admins can manage the entire catalogue, orders, and users from a dashboard.

> 🎓 Group project — Team of 4 | University of Transport and Technology (UTT)

---

## ✨ Features

### 👤 Customer
- Register, log in, and manage account
- Browse products by category (Electronics, Sports, Refrigerators, Cameras, etc.)
- Search and filter products
- Add / remove / update items in shopping cart with real-time total calculation
- Place orders and choose payment method (COD, Banking, MoMo, VNPay)
- Leave product reviews and ratings (1–5 stars)
- View order history and status

### 🛠️ Admin
- Manage products: add, edit, delete, upload images
- Manage categories and manufacturers
- View and update order status (pending → paid → shipping → completed / cancelled)
- Manage users and roles
- Post and manage news/announcements

---

## 🗂️ Project Structure

```
CHO-XANH/
├── config/         # Database connection configuration
├── controllers/    # Request handling & business logic (MVC)
├── models/         # Database queries and data access
├── views/          # HTML templates and UI pages
├── partials/       # Reusable UI components (header, footer, nav)
├── core/           # MVC core classes (Router, Controller, Model)
├── css/            # Stylesheets
├── images/         # Product and UI images
└── nhom.sql        # Full MySQL database dump
```

---

## 🗄️ Database Schema

The database (`nhom`) contains the following tables:

| Table | Description |
|---|---|
| `users` | Customer and admin accounts with roles |
| `products` | Product catalogue with price, stock, image |
| `categories` | Product categories |
| `nhasanxuat` | Manufacturers / suppliers |
| `carts` | Shopping cart per user |
| `cart_items` | Items inside each cart |
| `orders` | Customer orders with status tracking |
| `order_items` | Individual items within each order |
| `payments` | Payment records (COD, banking, MoMo, VNPay) |
| `reviews` | Product ratings and comments |
| `news` | News and announcements posted by admin |

---

## 🚀 Getting Started

### Requirements
- PHP 8.x
- MySQL / MariaDB
- Apache (XAMPP or WAMP recommended)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/nttuan235-max/CHO-XANH.git
   ```

2. **Move the project to your web server root**
   ```
   XAMPP: C:/xampp/htdocs/CHO-XANH
   WAMP:  C:/wamp64/www/CHO-XANH
   ```

3. **Import the database**
   - Open phpMyAdmin → Create a new database named `nhom`
   - Import `nhom.sql` into that database

4. **Configure the database connection**
   - Open `config/` and update your DB credentials:
   ```php
   define('DB_HOST', '127.0.0.1');
   define('DB_NAME', 'nhom');
   define('DB_USER', 'root');
   define('DB_PASS', '');
   ```

5. **Start the server and open in browser**
   ```
   http://localhost/CHO-XANH
   ```

### Default Admin Account
| Username | Password |
|---|---|
| admin | 22 |

> ⚠️ Change the admin password after first login.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | PHP 8.x |
| Frontend | HTML, CSS |
| Database | MySQL / MariaDB |
| Architecture | MVC (Model-View-Controller) |
| Local Server | XAMPP / WAMP |

---

## 👥 Team

| Name | Role |
|---|---|
| Tuấn | Database design, Shopping cart module, API integration |
| An | Frontend UI, Product listing |
| Minh | Order management, Admin dashboard |
| Cường | Authentication, Payment flow |

---

## 📄 License

This project was developed for academic purposes at the University of Transport and Technology (UTT).
