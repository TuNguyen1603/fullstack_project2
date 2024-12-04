# Storefront Backend Project

## Overview

This project is a backend API built using Node.js and PostgreSQL. The API provides functionality for managing a storefront, including user authentication, product listings, and order management.

---

## Prerequisites

Before setting up the project, ensure you have the following installed:

- **Node.js (v16.16)**: [Download Node.js](https://nodejs.org/dist/v16.16.0/node-v16.16.0-x64.msi)
- **PostgreSQL 15**
- **Databases**: Create two PostgreSQL databases:
  - `project2` (for development)
  - `project2test` (for testing)

---

## Setup Instructions

### Step 1: Install Dependencies

To install all required dependencies, run the following command in the project root:

```bash
yarn
# or
npm install
```

Key dependences:

## Express: For building the server and handling routes.

### npm install express

### npm install --save-dev @types/express

## TypeScript: For type safety and development

### npm install --save-dev typescript

## dotenv: For managing environment variables.

### npm install dotenv

## db-migrate: For database migrations

### npm install -g db-migrate

## cors: For enabling Cross-Origin Resource Sharing

### npm install cors

## bcrypt: For hashing passwords securely.

### npm install bcrypt

### npm install --save-dev @types/bcrypt

## nodemon: For automatically restarting the server during development

### npm install nodemon

## jsonwebtoken: For generating and verifying JSON Web Tokens (JWT)

### npm install jsonwebtoken

### npm install --save-dev @types/jsonwebtoken

## supertest: For testing API endpoints

### npm install supertest

### npm install --save-dev @types/supertest

Configure the Database

## db-migrate up

Create Environment Variables

## Create a .env file in the root directory and add the following

POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_DB=project2
POSTGRES_TEST_DB=project2test
POSTGRES_USER=postgres
POSTGRES_PASSWORD=Tuanquen1991@
ENV=dev
BCRYPT_PASSWORD=project2-hash-pash
SALT_ROUNDS=10
TOKEN_SECRET=tunv35

Build and Run the Application

## Build the project:

### npm run build

## Start the server:

### npm run start

--- The server will be accessible at http://127.0.0.1:3000.

To run tests, use the following command:

### npm run test

Ports

## Server: Runs on port 3000.

## Database: Runs on port 5432.
