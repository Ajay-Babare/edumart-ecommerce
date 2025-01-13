# eduMart - E-Commerce Platform

eduMart is a scalable, full-stack eCommerce platform designed for the education sector. Built with **Angular** for the front-end and **Spring Boot** for the back-end, eduMart allows users to browse and purchase educational products such as books, courses, and gadgets. The platform features a user-friendly interface, secure authentication, and seamless payment integration.

This repository contains the source code for both the **front-end** (Angular) and **back-end** (Spring Boot) of the eduMart eCommerce platform.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Key Features](#key-features)
- [Frontend & Backend Repositories](#frontend--backend-repositories)
- [Installation](#installation)
  - [Front-end Installation](#front-end-installation)
  - [Back-end Installation](#back-end-installation)
- [Running the Application](#running-the-application)
  - [Running the Front-end](#running-the-front-end)
  - [Running the Back-end](#running-the-back-end)
- [API Documentation](#api-documentation)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

eduMart is a full-stack eCommerce platform built to cater to the education sector. The platform is divided into two parts:
- **Frontend**: Developed using Angular to provide a responsive, user-friendly interface.
- **Backend**: Built with Spring Boot, which handles authentication, product management, and order processing.

Key features of eduMart include:
- Secure user authentication via **JWT**.
- Browse a variety of educational products like books, gadgets, and more.
- Manage shopping cart and orders.
- Admin panel for managing users, products, and orders.
- Secure payment gateway integration with **PayPal**.

---

## Tech Stack

### Front-end:
- **Angular** (v12+): For building dynamic, single-page applications.
- **Angular Material**: UI components for responsive design.
- **RxJS**: For handling asynchronous data and events.
- **Bootstrap** (optional): For flexible, mobile-first layout design.
- **JWT Authentication**: Secure user authentication with JSON Web Tokens.

### Back-end:
- **Spring Boot** (v2.5+): A Java-based framework to build RESTful APIs.
- **Spring Security**: For authentication and authorization (JWT-based).
- **Spring Data JPA**: For ORM-based database interaction.
- **MySQL**: Relational database for data storage.
- **Swagger**: For API documentation and testing (optional).
- **JUnit**: For unit and integration testing.

### Other:
- **PayPal Integration**: Secure payment processing.
- **Docker**: For containerizing the application (optional).

---

## Key Features

- **User Authentication**: 
  - Registration and login with JWT-based authentication.
  - Secure access control to different parts of the application.

- **Product Management**: 
  - Admins can manage the product catalog (Add, Edit, Delete Products).
  - Users can view product details, search, and filter.

- **Shopping Cart & Order Management**: 
  - Add items to the cart and manage quantities.
  - Place and view order history.

- **Payment Integration**: 
  - Seamless integration with **PayPal** for payment processing.

- **Admin Dashboard**: 
  - Admins can manage users, products, and track orders in real-time.

---

## Frontend & Backend Repositories

You can find the **source code** for both the **frontend** and **backend** of the eduMart platform at the following repository links:

- **Frontend Repository** (Angular):  
  [eduMart-frontend](https://github.com/Ajay-Babare/edumart-frontend)

- **Backend Repository** (Spring Boot):  
  [eduMart-backend](https://github.com/Ajay-Babare/edumart-backend)

---

## Installation

### Front-end Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Ajay-Babare/edumart-frontend.git
   cd eduMart-frontend

2. Install dependencies:
  `npm install`

3. Configure API URL in `src/environments/environment.ts`:
   ```javascript
   export const environment = {
    production: false,
    apiUrl: 'http://localhost:8080/api'  # Update this to match your backend URL
   };
  
4. Start the Angular development server:
  `ng serve`

5. Access the front-end at:
   `http://localhost:4200/`.
---
### Back-end Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Ajay-Babare/edumart-backend.git
   cd eduMart-backend

2. Install dependencies and build the project:
   `mvn clean install`

3. Configure database connection in `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/eduMart
   spring.datasource.username=root
   spring.datasource.password=password
   spring.jpa.hibernate.ddl-auto=update
   spring.security.jwt.secret=your-jwt-secret
   ```
4. Run the Spring Boot application:
   ```bash
   mvn spring-boot:run
   ```

5. `Access the back-end at:`
   http://localhost:8080/.
---
## Running the Application
### Running the Front-end
1. After setting up the front-end (as described above), run:
   ```bash
   ng serve

2. Access the app in your browser at:
   `http://localhost:4200/`.
---
### Running the Back-end
1. After setting up the back-end (as described above), run:
   ```bash
   mvn spring-boot:run
  
2. Access the back-end at `http://localhost:8080/`

---
## API Documentation
The back-end exposes the following API endpoints for communication with the front-end:

#### Authentication
- **POST /api/auth/register**: Register a new user.
- **POST /api/auth/login**: Log in and get a JWT token.
#### Products (Admin)
- **GET /api/products**: List all products.
- **POST /api/products**: Add a new product (Admin only).
- **PUT /api/products/{id}**: Edit an existing product (Admin only).
- **DELETE /api/products/{id}**: Delete a product (Admin only).
#### Cart
- **GET /api/cart**: Get current user's shopping cart.
- **POST /api/cart/add**: Add a product to the cart.
- **DELETE /api/cart/remove/{productId}**: Remove a product from the cart.
#### Orders
- **GET /api/orders**: Get all orders placed by the user.
- **POST /api/orders**: Place a new order.
---
## Testing
Unit Tests: Unit tests are included for both the front-end (using Jasmine/Karma) and back-end (using JUnit).
Integration Testing: Use Postman or Swagger UI to test API endpoints.

---
## Deployment
### Dockerization
1. Dockerize the back-end: Create a Dockerfile in the back-end project and build the Docker image.
2. Dockerize the front-end: Similarly, you can containerize the Angular front-end if needed.
3. Deploy on Cloud: Use AWS, Google Cloud, or Heroku for scalable production deployment.

## Contributing
We welcome contributions to eduMart! Here's how you can contribute:

1. Fork the repository.
2. Create a feature branch (git checkout -b feature/your-feature).
3. Make your changes and commit (git commit -m 'Add new feature').
4. Push your changes to your fork (git push origin feature/your-feature).
5. Open a pull request with a clear description of your changes.

## License
eduMart is licensed under the MIT License. See the LICENSE file for more information.
