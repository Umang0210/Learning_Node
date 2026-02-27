# Node Project (nodejs-1)

A beginner-friendly Node.js + Express project using ES Modules.

## Tech Stack

- Node.js
- Express
- Mongoose
- JSON Web Token (`jsonwebtoken`)
- bcrypt
- EJS

## Project Structure

- `index1.js` – current entry point (starts Express server)
- `config/db.js` – MongoDB connection helper
- `controllers/` – request handlers for users and products
- `models/` – sample in-memory data arrays
- `routes/` – user and product routes
- `middleware/` – auth and role-authorization middleware

## Prerequisites

- Node.js 18+ (recommended)
- npm
- MongoDB (local or remote)

## Installation

```bash
cd node
npm install
```

## Run the App

```bash
node index1.js
```

Server starts on:

- `http://localhost:8080`

## Current Status

At the moment, `index1.js` only starts the Express server. Route mounting, middleware usage, and DB connection are present in files but not yet wired into the running app.

## Available Route Modules (when mounted)

### Users

- `GET /` -> returns sample users (`controllers/userController.js`)
- `POST /` -> demo create-user response

### Products

- `GET /` -> returns sample products (`controllers/productController.js`)
- `POST /` -> demo add-product response

## Suggested Next Step

Wire routes and database in `index1.js`, for example:

- `app.use(express.json())`
- `app.use('/users', userRouter)`
- `app.use('/products', productRouter)`
- call `connectDB()` before `app.listen(...)`

---

If you want, I can also update `index1.js` now to fully connect routes + DB and add proper `start`/`dev` scripts in `package.json`.
