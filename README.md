#  Greencart - E-Commerce Grocery Platform

Greencart is a full-stack e-commerce platform designed for grocery shopping, featuring a modern React frontend and a robust Node.js/Express backend. The platform supports both customer and seller functionalities, including product management, shopping cart, order processing, and secure payment integration.

## Features

### Customer Features
-  User authentication (login/register)
-  Browse products by category
-  Product search and filtering
-  Shopping cart management
-  Address management
-  Secure payment processing with Stripe
-  Order history and tracking
-  Responsive design for all devices

### Seller Features
-  Seller dashboard
-  Add and manage products
-  View and manage orders
-  Image upload with Cloudinary integration
-  Product inventory management

##  Tech Stack

### Frontend
- **React 19** - UI library
- **Vite** - Build tool and dev server
- **Tailwind CSS** - Styling framework
- **React Router DOM** - Client-side routing
- **Axios** - HTTP client
- **React Hot Toast** - Toast notifications

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database (with Mongoose ODM)
- **JWT** - Authentication
- **Bcryptjs** - Password hashing
- **Stripe** - Payment processing
- **Cloudinary** - Image storage and management
- **Multer** - File upload handling
- **CORS** - Cross-origin resource sharing

##  Project Structure

```
greencart/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # Reusable React components
│   │   ├── pages/          # Page components
│   │   ├── context/       # React context for state management
│   │   ├── assets/         # Images and static assets
│   │   └── App.jsx         # Main App component
│   ├── public/             # Public assets
│   └── package.json
│
├── server/                 # Backend Node.js application
│   ├── configs/           # Configuration files (DB, Cloudinary, Multer)
│   ├── controllers/        # Route controllers
│   ├── middlewares/        # Authentication middlewares
│   ├── models/             # MongoDB models
│   ├── routes/             # API routes
│   ├── server.js           # Entry point
│   └── package.json
│
└── README.md
```

##  Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or cloud instance like MongoDB Atlas)
- npm or yarn package manager
- Stripe account (for payment processing)
- Cloudinary account (for image storage)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/romil45/Green
   cd greencart
   ```

2. **Install server dependencies**
   ```bash
   cd server
   npm install
   ```

3. **Install client dependencies**
   ```bash
   cd ../client
   npm install
   ```

### Environment Variables

Create a `.env` file in the `server` directory with the following variables:

```env
# Server Configuration
PORT=4000

# Database
MONGODB_URI=your_mongodb_connection_string

# JWT Secret
JWT_SECRET=your_jwt_secret_key

# Cloudinary Configuration
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# Stripe Configuration
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
```

### Running the Application

1. **Start the backend server**
   ```bash
   cd server
   npm start
   # or for development with auto-reload
   npm run server
   ```
   The server will run on `http://localhost:4000`

2. **Start the frontend development server**
   ```bash
   cd client
   npm run dev
   ```
   The client will run on `http://localhost:5173`
   
3. ** to open admin panal**
http://localhost:5173/seller

SELLER_EMAIL = "admin@example.com"

SELLER_PASSWORD = "greatstack123"
   

##  API Endpoints

### User Routes (`/api/user`)
- `POST /register` - Register a new user
- `POST /login` - User login
- `GET /profile` - Get user profile
- `POST /logout` - User logout

### Product Routes (`/api/product`)
- `GET /list` - Get all products
- `GET /:id` - Get product by ID
- `GET /category/:category` - Get products by category

### Cart Routes (`/api/cart`)
- `POST /add` - Add item to cart
- `POST /remove` - Remove item from cart
- `GET /get` - Get cart items

### Address Routes (`/api/address`)
- `POST /add` - Add new address
- `GET /list` - Get user addresses
- `DELETE /:id` - Delete address

### Order Routes (`/api/order`)
- `POST /place` - Place a new order
- `GET /list` - Get user orders
- `POST /stripe` - Stripe webhook endpoint

### Seller Routes (`/api/seller`)
- `POST /register` - Register a new seller
- `POST /login` - Seller login
- `POST /add-product` - Add a new product
- `GET /products` - Get seller's products
- `GET /orders` - Get seller's orders

## Author

Romil Moradiya - [https://github.com/romil45/Green]
