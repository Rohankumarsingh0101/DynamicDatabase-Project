# DynamicDatabase-Project
# DynamicDatabase Project

## 📌 Overview
This is a Node.js-based REST API project using Express.js and MongoDB. It follows a structured architecture by separating concerns into different folders such as models, controllers, routes, and configurations.

## 📂 Folder Structure
```
/DynamicDatabase
│── config/
│   ├── db.js  --> Database connection setup
│
│── middlewares/
│   ├── corsMiddleware.js  --> Middleware for CORS handling
│
│── models/
│   ├── user.js  --> Mongoose schema for users
│
│── controllers/
│   ├── userController.js  --> Handles API logic (CRUD operations)
│
│── routes/
│   ├── userRoutes.js  --> Defines routes and connects to controllers
│
│── server.js  --> Main entry point for the application
│── package.json
│── package-lock.json
│── README.md
```

## 🚀 Getting Started

### 1️⃣ Prerequisites
Make sure you have the following installed:
- [Node.js](https://nodejs.org/) (v18 or later recommended)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas Cloud Database)

### 2️⃣ Installation
Clone the repository and install dependencies:
```sh
# Clone the repo
git clone https://github.com/your-username/DynamicDatabase.git
cd DynamicDatabase

# Install dependencies
npm install
```

### 3️⃣ Configure Environment
Set up your MongoDB connection in `config/db.js`:
```js
const mongoose = require("mongoose");

mongoose.connect("mongodb://127.0.0.1:27017/DynamicDatabase", {
  useNewUrlParser: true,
  useUnifiedTopology: true,
})
.then(() => console.log("MongoDB connected"))
.catch((err) => console.log("MongoDB connection error:", err));

module.exports = mongoose;
```

### 4️⃣ Running the Server
Start the server with Nodemon (for auto-reloading):
```sh
npm install -g nodemon
nodemon server.js
```
Or run without Nodemon:
```sh
node server.js
```

## 🛠 API Endpoints

### 📌 User Routes
| Method | Endpoint       | Description |
|--------|--------------|-------------|
| GET    | `/users`       | Fetch all users |
| POST   | `/users`       | Create a new user |
| PUT    | `/users/:id`   | Update a user by ID |
| DELETE | `/users/:id`   | Delete a user by ID |

## 💡 Features
✅ Modular and scalable structure
✅ MongoDB integration using Mongoose
✅ Express.js for handling RESTful APIs
✅ Middleware support (CORS, JSON parsing)
✅ CRUD operations for user management

## 🏗 Future Improvements
- Implement authentication (JWT)
- Add input validation using Joi
- Use `.env` for sensitive configurations

## 👨‍💻 Contributors
- **Rohan kumar Singh** -[ Github name: Rohankumarsingh0101 (https://github.com/Rohankumarsingh0101)

## 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

---

Made with ❤️ by Rs

