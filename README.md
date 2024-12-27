# Project Overview

This project is a **web application** built with **Node.js**, **Express**, and **MongoDB**. It allows users to manage listings (e.g., hotels, apartments) with features like creating, viewing, updating, and deleting listings, as well as leaving reviews.

## Key Features

### 1. **CRUD Operations**
The core functionality is based around **CRUD** (Create, Read, Update, Delete) operations. Users can:
- **Create** new listings with details (e.g., name, description, price).
- **Read** and view existing listings in detail.
- **Update** listings with changes to information like price, description, etc.
- **Delete** listings that are no longer needed.

### 2. **Review System**
- Users can leave **reviews** for listings, including a text description and a rating (1-5 stars).
- Reviews are tied to specific listings, allowing users to give detailed feedback.
- Users can also **delete** their reviews at any time.

### 3. **Form Validation**
To ensure the integrity and security of submitted data, the app uses **Joi** for input validation:
- Validates form data to prevent malicious or invalid entries.
- Provides **detailed error messages** if input does not meet validation criteria (e.g., invalid email format or missing required fields).

### 4. **MongoDB and Mongoose**
- **MongoDB** serves as the database to store user information, listings, and reviews.
- **Mongoose** is used as an **ODM** (Object Document Mapper) to interact with MongoDB, allowing for easy data modeling, querying, and validation.

### 5. **Dynamic Views with EJS**
- The app uses **EJS** (Embedded JavaScript) for dynamic HTML rendering.
- Views like listing details, user reviews, and forms are generated dynamically based on database data.

### 6. **Error Handling**
The application includes a custom error handling system using the `ExpressError` class:
- Manages errors by sending appropriate error messages and status codes.
- Catches and handles issues such as invalid routes, missing data, and incorrect actions for a smoother user experience.

### 7. **Middleware**
The app utilizes middleware to enhance functionality:
- **Method-Override** middleware allows handling HTTP methods (PUT, DELETE) in forms, despite browsers supporting only GET and POST natively. This enables users to update and delete listings/reviews.

### 8. **Security Measures**
- Implements security practices like input sanitization and validation to prevent common vulnerabilities like **SQL injection** and **XSS** (Cross-Site Scripting).
- Uses **Helmet** and **CORS** to secure HTTP headers and handle cross-origin requests.

## Technologies Used

- **Node.js**: JavaScript runtime for building the server-side of the application.
- **Express**: Web application framework for routing and middleware handling.
- **MongoDB**: NoSQL database used for storing listings, reviews, and user data.
- **Mongoose**: ODM for MongoDB to handle data modeling and querying.
- **EJS**: Template engine for rendering dynamic HTML views.
- **Joi**: Data validation library to ensure proper form submissions.
- **Method-Override**: Middleware to support PUT and DELETE methods in forms.
