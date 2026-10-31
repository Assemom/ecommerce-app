# DEPI Final Project — E-Commerce App

Full-stack e-commerce application built as the Digital Egypt Pioneers Initiative (DEPI) final project.

## 👥 Team

Remon, Assem, Mahmoud Fares and Mohammed el bahrawy

## 🛠 Tech Stack

| Layer    | Technologies |
|----------|--------------|
| Frontend | React 18, Redux Toolkit, React Router, Axios, Tailwind CSS, Radix UI, Framer Motion, Vite |
| Backend  | Node.js, Express, MongoDB (Mongoose), JWT authentication, Cloudinary file storage |
| Tools    | Git, GitHub, npm, ESLint, Prettier |

## 📁 Project Structure

```
├── Backend/     # Express REST API
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   └── app.js
├── Frontend/    # React + Vite SPA
│   ├── public/
│   └── src/
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18+)
- A MongoDB database (local or [Atlas](https://www.mongodb.com/atlas))
- A [Cloudinary](https://cloudinary.com/) account (for product image uploads)

### 1. Clone the repository

```bash
git clone https://github.com/Assemom/ecommerce-app.git
cd ecommerce-app
```

### 2. Backend setup

```bash
cd Backend
npm install
```

Create a `.env` file in the `Backend/` folder:

```env
PORT=3000
MONGODB_CONNECTION=<your-mongodb-connection-string>
JWT_SECRET_KEY=<your-jwt-secret>
CLOUDINARY_CLOUD_NAME=<your-cloudinary-cloud-name>
CLOUDINARY_API_KEY=<your-cloudinary-api-key>
CLOUDINARY_API_SECRET=<your-cloudinary-api-secret>
FRONTEND_URL=http://localhost:5173
```

Run the dev server:

```bash
npm run dev
```

The API starts on [http://localhost:3000](http://localhost:3000). Health check: `GET /health`.

### 3. Frontend setup

Open a new terminal from the project root:

```bash
cd Frontend
npm install
```

Create a `.env` file in the `Frontend/` folder:

```env
VITE_API_BASE_URL=http://localhost:3000/api
```

Run the dev server:

```bash
npm run dev
```

The app opens at [http://localhost:5173](http://localhost:5173).

### 🏗 Production build (Frontend)

```bash
npm run build
npm run preview
```

## 🔌 API Overview

All endpoints are prefixed with `/api`.

| Endpoint       | Description                              |
|----------------|------------------------------------------|
| `/api/users`   | Authentication & user management         |
| `/api/products`| Product browsing, search & CRUD          |
| `/api/categories` | Category browsing & CRUD              |
| `/api/orders`  | Order creation & tracking                |
| `/api/reviews` | Product reviews & ratings                |

Unknown routes return a `404` JSON error. A global error handler keeps the API resilient to invalid requests.

## 📄 License

This project was created for educational purposes as part of the DEPI program.
