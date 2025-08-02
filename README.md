🛒 OneCart – MERN E-Commerce Platform

*OneCart* is a complete fashion-centric e-commerce web application built using the *MERN stack*. It features a responsive frontend for customers, a secure admin dashboard, and a scalable backend API — all designed to simulate real-world e-commerce systems during a hands-on virtual internship.

---

## 🧩 Key Features

- 🛍 *Fashion-Focused UI* – Bold homepage with curated collections
- 🛒 *Cart Management* – Add to cart, remove, total calculation
- 🧑‍💼 *Admin Panel* – Add/delete products via a protected dashboard
- 🔐 *Secure Routing* – Backend API secured with route-level protection
- 📦 *Product Categories* – Categorized product listing for easy browsing
- 🔄 *Order Flow (WIP)* – Cart to checkout with order placeholders
- ⚡ *Fast UX* – Vite-powered frontend and admin dashboard
- 🌐 *Seamless Architecture* – Frontend, admin, and backend are modular

---

## 🏗 Technical Architecture

### Frontend (React + Vite)

- Built using React with Vite bundler for blazing-fast performance
- Uses *Context API* for state (cart, auth)
- Components: Nav, Card, Hero, Footer, CategoryBanner, etc.
- Firebase setup ready for user auth
- Responsive mobile-first design

### Admin (React + Vite)

- Separate admin dashboard app
- Add new products with image, price, category, and description
- Delete products with one click
- Clean and modern dashboard UI

### Backend (Node.js + Express)

- RESTful API built with Express.js
- Mongoose + MongoDB for database
- Product and user model setup
- Protected routes for admin
- Environment-based config system

---

## 🧠 Design Decisions

### Modular Foldering

Each app (frontend, backend, admin) is separate — scalable for large production systems.

### Vite over CRA

Vite ensures fast hot module replacement and dev build time.

### Context API vs Redux

Lightweight Context API was used instead of Redux for simplicity and speed.

### Secure Backend Routing

Admin routes are separated and protected for future JWT-based auth.

---

## 🗃 Project Structure

text
onecart/
├── frontend/                # Customer-facing React app
│   ├── public/              # Static files (index.html, favicon, etc.)
│   ├── src/
│   │   ├── assets/          # Images, logos, media
│   │   ├── component/       # UI components (Nav, Footer, Cards)
│   │   ├── context/         # AuthContext, CartContext
│   │   ├── pages/           # Home, Collections, Cart, Product, etc.
│   │   ├── utils/           # Firebase config, helpers
│   │   ├── App.jsx          # Root component
│   │   └── main.jsx         # App entry point
│   ├── .gitignore
│   ├── package.json
│   ├── vite.config.js
│   └── index.html

├── admin/                  # Admin Panel
│   ├── public/
│   ├── src/
│   │   ├── components/      # ProductForm, DashboardLayout, Sidebar
│   │   ├── pages/           # ManageProducts, AddProduct, etc.
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── .gitignore
│   ├── package.json
│   ├── vite.config.js
│   └── index.html

├── backend/               # Backend Server (Express)
│   ├── config/             # DB config
│   ├── controller/         # Logic for product routes
│   ├── middleware/         # Auth middleware (WIP)
│   ├── model/              # Mongoose schemas
│   ├── routes/             # Express routes
│   ├── public/             # Public assets (optional)
│   ├── index.js            # Server entry point
│   ├── .gitignore
│   └── package.json

└── README.md              # Root project documentation


## ⚙ Setup Instructions

### Prerequisites

- Node.js (v14+)
- MongoDB
- npm or yarn

---

### 🖥 Backend Setup

bash
cd backend
npm install
Create a .env file with:

PORT=5000
MONGO_URI=your_mongodb_connection_string
Then start the server:


npm start
API runs on: http://localhost:5000

💻 Frontend Setup

cd frontend
npm install
npm run dev
Runs at: http://localhost:5173

🧑‍💼 Admin Panel Setup

cd admin
npm install
npm run dev
Runs at: http://localhost:5174

📡 API Endpoints
Products
GET /api/products – Get all products

POST /api/products – Add a new product (admin)

DELETE /api/products/:id – Delete product (admin)

Users (Coming Soon)
POST /api/auth/register

POST /api/auth/login

🛠 Technologies Used
Frontend & Admin
React.js

Vite

React Router

Context API

Firebase (Auth Ready)

Tailwind / CSS

Backend
Node.js

Express.js

MongoDB

Mongoose

dotenv

🚀 Future Enhancements
🔐 JWT-based user authentication

💳 Razorpay or Stripe integration

⭐ Product rating & review system

📦 Order history & user profile

📈 Admin analytics dashboard

📱 Mobile responsive PWA

👨‍💻 Contributors
Rajesh Sharma – Full Stack Developer
