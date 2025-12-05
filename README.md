# Complaint Management System

A full-stack web application for submitting, tracking, and resolving complaints.
Built with **Node.js**, **Express**, **GraphQL**, **MongoDB**, and a **React frontend** using **Apollo Client**, **Material-UI**, and **React Router**.

---

## Prerequisites

* Node.js (v14 or later recommended)
* npm
* MongoDB (local or cloud)

---

## 1. Clone the Repository

```sh
git clone https://github.com/manasdekivadia/CMS---Complaint-Management-System.git
cd CMS---Complaint-Management-System
```

---

## 2. Backend Setup

```sh
cd backend
npm install
```

Create a `.env` file in `backend/`:

```
PORT=5000
UI_URL=http://localhost:3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

Start the backend:

```sh
npm start
```

Backend GraphQL endpoint:

```
http://localhost:5000/graphql
```

---

## 3. Frontend Setup

```sh
cd ../frontend
npm install
npm start
```

Frontend runs at:

```
http://localhost:3000
```

Authentication is cookie-based (JWT).
Routing adapts to user role:

* **Student:** `/complaints`, `/complaints/me`, `/create`, `/givefeedback`
* **Dean:** `/view`, `/resolve`
* **Unauthenticated:** `/login`, `/signup`

---

## 4. Usage

1. Run both backend and frontend.
2. Navigate to `http://localhost:3000`.
3. Register or log in.

**Students can:**

* Submit complaints
* View all complaints
* Track their own complaints
* Submit feedback

**Dean role can:**

* Review complaints
* Resolve complaints
* View student feedback

---

## 5. Tech Stack

### Backend

* Node.js + Express
* GraphQL (`express-graphql`)
* MongoDB + Mongoose
* JWT authentication
* CORS & cookie parsing
* Role-based access system

### Frontend

* React 18
* React Router v6
* Apollo Client
* Material-UI v4 + MUI v5 icons
* JWT decode + cookie authentication

---

## 6. Development Scripts

### Backend

```sh
npm start
npm run dev
```

### Frontend

```sh
npm start
npm run build
```

---

## 7. Notes

* Frontend communicates with backend at `/graphql` on **port 5000**.
* Ensure `.env` is properly configured before starting the backend.
* Cookies must be enabled for authentication to work.
* If frontend installation shows peer-dependency errors (React 18 + Material-UI v4), install with:

  ```sh
  npm install --legacy-peer-deps
  ```

---

.


