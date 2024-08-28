# Food Delivery App

## Overview

This is a full-stack food delivery application built using the MERN stack (MongoDB, Express, React, Node.js). The application includes three main parts: the frontend, the backend, and the admin panel. It also integrates Stripe for payment processing and includes authentication features.

## Deployment
The application is deployed https://food-dev-frontend.onrender.com/

## Folder Structure

- **frontend**: Contains the React application for the user interface.
- **backend**: Contains the Node.js server and Express application for handling API requests.
- **admin**: Contains the React application for the admin panel.

## Features

### User Features

- **User Authentication**:
  - **Signup**: Users can create a new account by providing their name, email and password.
  - **Login**: Existing users can log in using their email and password.
  - **JWT Authentication**: Secure user sessions with JSON Web Tokens (JWT).


- **Browsing Food Items**:
  - **Menu Display**: Users can view a list of available food items, including details such as name, description, price, and image.

- **Cart Management**:
  - **Add to Cart**: Users can add food items to their cart.
  - **Remove from Cart**: Users can remove food items from their cart.
  - **Cart Summary**: Users can view a summary of their cart, including total items and total price.

- **Order Placement**:
  - **Address Form**: Users provide delivery address details.
  - **Payment Integration**: Secure payment processing using Stripe..

- **Order History**:
  - **View Orders**: Users can view a list of their past orders.
  - **Order Details**: Users can view detailed information about each order, including items ordered, quantity, total amount, and delivery status.

### Admin Features

- **Food Item Management**:
  - **Add Food Item**: Admins can add new food items to the menu, providing details such as name, description, price, and image.
  - **Delete Food Item**: Admins can remove food items from the menu.

- **Order Management**:
  - **View All Orders**: Admins can view a list of all orders placed by users.
  - **Order Details**: Admins can view detailed information about each order.
  - **Update Order Status**: Admins can update the status of orders (e.g., processing, delivered).

## Technologies Used

- **Frontend**: React, Axios, React Router, Context API
- **Backend**: Node.js, Express.js, MongoDB, Mongoose, JWT for authentication
- **Payment Gateway**: Stripe
- **Styling**: CSS

## Installation

### Prerequisites

- Node.js
- MongoDB
- Stripe account for payment processing

### Backend


1. Install the dependencies:
   ```bash
   npm install
   ```

2. Create a `.env` file in the backend directory with the following environment variables:
   ```env
   MONGODB_URI=your_mongodb_uri
   JWT_SECRET=your_jwt_secret
   STRIPE_SECRET_KEY=your_stripe_secret_key
   URL=frontend_url
   ```

3. Start the backend server:
   ```bash
   npm start
   ```

### Backend

1. Install the dependencies:
   ```bash
   npm install
   ```

2. Change the backend url in StoreContext file

3. Start the backend server:
   ```bash
   npm start
   ```


## Usage

### User Authentication

- Users can sign up and log in to the application.
- Authentication is managed using JWT.

### Browsing and Ordering

- Users can browse the menu, add items to their cart, and place orders.
- Orders are processed using Stripe for payment.

### Admin Panel

- Admins can log in to the admin panel to manage food items and view orders.
- The admin panel provides functionalities to add, update, and delete food items.

## API Endpoints

### User

- `POST /api/user/signup`: Sign up a new user
- `POST /api/user/login`: Log in an existing user

### Orders

- `POST /api/order/place`: Place a new order
- `GET /api/order/list`: Get a list of all orders (admin only)
- `GET /api/order/userorders`: Get a list of orders for a specific user

### Food Items

- `GET /api/food`: Get a list of food items
- `POST /api/food/add`: Add a new food item (admin only)
- `PUT /api/food/update/:id`: Update a food item (admin only)
- `DELETE /api/food/delete/:id`: Delete a food item (admin only)

