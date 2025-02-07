# ecommerce-mern
# **Full Stack MERN E-commerce Platform**  

## **Project Overview**  
The **Full Stack MERN E-commerce Platform** is a web application that allows users to browse products, add them to their cart, place orders, and optionally make payments using Razorpay. It includes an admin panel (bonus feature) for managing products and tracking orders.  

This document outlines the **features, technology stack, and detailed requirements** for the development of the platform.  

---

## **Technology Stack**  

### **Frontend (Client-side)**  
- **React.js** – For building the user interface.  
- **React Router** – For handling navigation between pages.  
- **Redux Toolkit** – For managing global state efficiently.  
- **Ant Design** – UI component library for styling and responsive layouts.  
- **Axios** – For making API requests to the backend.  

### **Backend (Server-side)**  
- **Node.js** with **Express.js** – For handling API requests and server-side logic.  
- **PostgreSQL** – Relational database for storing structured data.  
- **Sequelize** – ORM for managing database interactions.  
- **JWT (JSON Web Token)** – For secure user authentication and authorization.  
- **Bcrypt.js** – For password hashing to enhance security.  

### **Payment Gateway (Optional)**  
- **Razorpay** – For handling secure online transactions.  

---

## **User Roles**  

### **1. Customer (Regular User)**  
- Can **browse** and **view products**.  
- Can **add products to the cart** and **place orders**.  
- Can **view order history** and track order status.  
- Can **make payments** (if enabled).  

### **2. Admin (Bonus Feature)**  
- Has access to an **admin panel**.  
- Can **manage products** (add, update, delete).  
- Can **view and manage orders** (update order status).  

---

## **Features & Functionalities**  

### **1. User Authentication**  
- Users must be able to **register and log in** using an email and password.  
- Authentication will be handled using **JWT tokens**.  
- Passwords must be securely **hashed** before being stored.  

---

### **2. Product Management**  

#### **For Customers:**  
- View a **list of available products**, including **name, price, and image**.  
- Click on a product to **view detailed information**, such as **description, stock availability, and additional images**.  
- Products should be **categorized** for easy navigation.  

#### **For Admins (Bonus Feature):**  
- Admins can **add, update, and delete products** from the system.  
- The product management interface should allow **bulk product uploads** (CSV upload optional).  
- Products should have **stock levels** that update when an order is placed.  

---

### **3. Shopping Cart & Order Placement**  

#### **For Customers:**  
- Add **products to a cart** and adjust quantities.  
- The cart should persist between sessions (stored locally or in the database).  
- Proceed to **checkout**, where users can:  
  - Review their **order summary**.  
  - Enter their **shipping details**.  
  - Confirm their **order**.  
- After placing an order, the user should:  
  - Receive an **order confirmation**.  
  - Be able to **track their order** and view its current status (e.g., Processing, Shipped, Delivered).  

#### **For Admins (Bonus Feature):**  
- Admins can **view all orders** placed on the platform.  
- Orders should be **filtered by status** (Processing, Shipped, Delivered).  
- Admins can **update order status** as the order progresses.  

---

### **4. Payment Integration (Optional)**  
- Users should have an option to **pay online** using Razorpay.  
- Payments can be made via **UPI, credit/debit card, or net banking**.  
- If payment integration is enabled, an order should be marked as **confirmed only after successful payment**.  

---

## **Admin Panel (Bonus Feature)**  

### **Admin Features**  
- A **secure login system** for admin access.  
- A **dashboard** displaying:  
  - Total sales revenue.  
  - Recent orders.  
  - Number of pending and completed orders.  
- **Product Management:**  
  - Admins can **add, edit, and delete products**.  
  - Stock levels should be updated when an order is placed.  
- **Order Management:**  
  - View **all orders** in a tabular format.  
  - Update **order status** to Processing, Shipped, or Delivered.  

---

## **Non-Functional Requirements**  
- The system should be **secure**, with **hashed passwords** and JWT-based authentication.  
- The UI should be **responsive and mobile-friendly** using Ant Design.  
- The database should be **efficiently structured** to support future scalability.  
- API responses should be **optimized for performance** with proper indexing and caching.  
- The system should handle **concurrent orders and updates** without inconsistencies.  

---

This document serves as a **detailed requirement specification** for building the **Full Stack MERN E-commerce Platform** with PostgreSQL and Ant Design.