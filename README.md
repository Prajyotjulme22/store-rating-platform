# Store Rating Platform

## Overview

Store Rating Platform is a full-stack web application that enables users to discover stores, submit ratings, and manage store information through a secure role-based system. The platform supports three user roles: System Administrator, Store Owner, and Normal User.

The application is designed using modern web development practices, secure authentication, responsive user interfaces, and scalable database architecture.

---

## Key Features

### System Administrator

* Manage users and stores
* Create Admin, Store Owner, and Normal User accounts
* View platform statistics
* Monitor total users, stores, and ratings
* Filter and search users and stores
* Access detailed user information

### Normal User

* Register and log in securely
* Browse all available stores
* Search stores by name or address
* Submit ratings from 1 to 5 stars
* Update previously submitted ratings
* Change account password

### Store Owner

* Access store dashboard
* View average store rating
* Monitor customer feedback
* View users who rated the store
* Update account password

---

## Technology Stack

### Frontend

* React.js
* React Router DOM
* Axios
* Bootstrap / CSS

### Backend

* Express.js
* Node.js
* JWT Authentication
* bcrypt Password Encryption

### Database

* PostgreSQL / MySQL
* Sequelize ORM

---

## Project Architecture

```text
store-rating-platform/

├── Backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── scripts/
│   └── server.js
│
├── Frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       └── utils/
│
└── README.md
```

---

## Database Design

### Users

| Field    | Type                 |
| -------- | -------------------- |
| id       | Integer              |
| name     | String               |
| email    | String               |
| password | String               |
| address  | String               |
| role     | ADMIN / USER / OWNER |

### Stores

| Field   | Type    |
| ------- | ------- |
| id      | Integer |
| name    | String  |
| email   | String  |
| address | String  |
| ownerId | Integer |

### Ratings

| Field   | Type          |
| ------- | ------------- |
| id      | Integer       |
| userId  | Integer       |
| storeId | Integer       |
| rating  | Integer (1-5) |

---

## Form Validation Rules

### Name

* Minimum 20 characters
* Maximum 60 characters

### Email

* Must follow valid email format

### Password

* Minimum 8 characters
* Maximum 16 characters
* At least one uppercase letter
* At least one special character

### Address

* Maximum 400 characters

### Rating

* Value between 1 and 5

---

## Installation

### Clone Repository

```bash
git clone https://github.com/Prajyotjulme22/store-rating-platform/tree/main
cd store-rating-platform
```

### Backend Setup

```bash
cd Backend

npm install

npm run dev
```

### Frontend Setup

```bash
cd Frontend

npm install

npm run dev
```

---

## Environment Variables

```env
PORT=5000

DB_HOST=localhost
DB_PORT=5432
DB_NAME=rating_system
DB_USER=postgres
DB_PASSWORD=your_password

JWT_SECRET=your_secret_key
```

---

## Security Features

* JWT Authentication
* Password Hashing using bcrypt
* Role-Based Access Control
* Protected Routes
* Input Validation
* Secure API Endpoints

---

## Future Enhancements

* Email Verification
* Password Reset via Email
* Store Images Upload
* Admin Analytics Charts
* Review Comments System
* Mobile Application Support

---

## Author

Prajyot Julme

Full Stack Developer | React.js | Node.js | Express.js | PostgreSQL | MySQL
