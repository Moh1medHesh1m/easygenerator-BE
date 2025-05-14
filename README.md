<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## 📌 Description
The **Easy Generator API** is a production-ready backend built using **NestJS**, providing **secure authentication**, **efficient data handling**, and **containerized deployment**.

It features **JWT-based authentication**, **unit testing**, **Redis caching**, and **MongoDB integration**.

### 🚀 Features
- **Modular Architecture** → Scalable NestJS module-based structure.
- **Authentication with Passport.js** → Secure JWT-based authentication.
- **Unit Testing with Jest** → Ensures reliability and correctness.
- **Redis Caching** → Optimized session handling and token blacklisting.
- **MongoDB Integration** → Uses Mongoose ORM for efficient data management.
- **Input Validation** → Request validation using `class-validator`.
- **Logging with Winston** → Centralized logging for debugging and monitoring.
- **Environment Configuration** → Uses `@nestjs/config` for easy management.
- **Docker Support** → Includes `Dockerfile` and `docker-compose` for containerization.

---

## 📌 Environment Variables
The application relies on environment variables for configuration. The most important variables include:

### **Server Configuration**
- `PORT`

### **Database Configuration**
- `DATABASE_URL`

### **Authentication**
- `JWT_SECRET`
- `JWT_EXPIRATION`

### **Redis Configuration**
- `REDIS_HOST`
- `REDIS_PORT`
- `REDIS_PASSWORD`

Refer to `.env.example` for required configurations.

---

## 📌 Authentication with Passport Strategy
The API uses **Passport.js strategies** for authentication:

- **JWT Strategy** → Secure authentication via JWT tokens.
- **Local Strategy** → Handles login with email and password.

This ensures **secure authentication and session handling**.

---

## 📌 Testing
The project includes **unit tests and e2e tests** to ensure functionality.

---
## 📌 API Documentation

The Easy Generator API provides interactive API documentation using **Swagger**.

You can access it at:
[https://easygenerator-be-qmmr.onrender.com/api/swagger](https://easygenerator-be-qmmr.onrender.com/api/swagger)

### 🚦 Available Endpoints

#### ✅ Public Endpoints
- **GET** `/api` → Base route
- **POST** `/api/auth/register` → Register a new user
- **POST** `/api/auth/login` → User login (returns JWT token)

#### 🔒 Protected Endpoints
- **GET** `/api/user/user-info` → Get user information (**requires Bearer JWT token** in the `Authorization` header)

### 🔑 How to Authorize in Swagger
1. Click the **Authorize** button in the top right of the Swagger UI.
2. Enter your JWT token  Do not include "Bearer"
3. Once authorized, you can test all protected routes directly from Swagger.

---

## 📌 Docker Support & Commands
The project supports **Docker containerization** using:

- **Dockerfile** → Builds a self-contained image of the application.
- **docker-compose.yml** → Sets up Redis, and the API.

### **Run the App with Docker**
```bash
docker-compose up --build
```

### **Stop Containers**

```bash
docker-compose down
```

### **Check Running Containers**

```bash
docker ps
```

### **View Logs**

```bash
docker logs <container_id>
```

## 📌 MongoDB Commands

**To interact with MongoDB inside Docker, use the following commands:**

## 1️⃣ Open MongoDB Shell

### **Run this command to access the MongoDB container:**

```bash
docker exec -it mongo mongosh -u admin -p password --authenticationDatabase admin
```
### Replace admin and password with the actual credentials used in docker-compose.yml.

## **2️⃣ View Available Databases**

```bash
show dbs;
```

## 3️⃣ **Switch to Your Database**

### Replace mydatabase with your actual database name:

```bash
use mydatabase;
```

## 4️⃣ **List Collections**
```bash
show collections;
```

## 5️⃣ **View Data Inside a Collection**

### Retrieve all documents from a collection (e.g., users):
```bash
db.users.find().pretty();
```
Replace users with the actual collection name.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).
