# BloodOnation - Blood Donation Management System

A full-stack web application for managing blood donation requests and connecting donors with recipients.

## Features

- User authentication (JWT-based)
- Role-based access control (Donor, Recipient, Admin)
- Blood donation request management
- User profile management
- Responsive Material-UI design

## Prerequisites

Before running the application, make sure you have the following installed:

- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm (v6 or higher)

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/bloodonation.git
cd bloodonation
```

### 2. Install Backend Dependencies

```bash
# From the root directory
npm install
```

### 3. Install Frontend Dependencies

```bash
# Navigate to client directory
cd client
npm install
```

### 4. Environment Variables

Create a `.env` file in the root directory:

```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/bloodonation
JWT_SECRET=your_jwt_secret_key
```

Create a `.env` file in the client directory:

```env
REACT_APP_API_URL=http://localhost:5000/api
```

## Running the Application

### 1. Start MongoDB

Make sure MongoDB is running on your system:

```bash
# Windows (if MongoDB is not running as a service)
"C:\Program Files\MongoDB\Server\{version}\bin\mongod.exe"

# Linux/Mac
mongod
```

### 2. Start the Backend Server

```bash
# From the root directory
npm run dev
```

### 3. Start the Frontend Development Server

```bash
# From the client directory
cd client
npm start
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## Project Structure

```
bloodonation/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── services/      # API services
│   │   ├── store/         # Redux store and slices
│   │   └── App.tsx        # Main application component
│   └── package.json       # Frontend dependencies
├── server/                 # Backend Node.js application
│   ├── controllers/       # Route controllers
│   ├── models/           # MongoDB models
│   ├── routes/           # API routes
│   └── middleware/       # Custom middleware
├── package.json          # Backend dependencies
└── README.md            # Project documentation
```

## Dependencies

### Backend Dependencies
```json
{
  "dependencies": {
    "bcryptjs": "^2.4.3",
    "cors": "^2.8.5",
    "dotenv": "^16.0.3",
    "express": "^4.18.2",
    "jsonwebtoken": "^9.0.0",
    "mongoose": "^7.0.3"
  },
  "devDependencies": {
    "nodemon": "^2.0.22"
  }
}
```

### Frontend Dependencies
```json
{
  "dependencies": {
    "@emotion/react": "^11.10.6",
    "@emotion/styled": "^11.10.6",
    "@mui/icons-material": "^5.11.16",
    "@mui/material": "^5.12.0",
    "@reduxjs/toolkit": "^1.9.3",
    "axios": "^1.3.5",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-redux": "^8.0.5",
    "react-router-dom": "^6.10.0",
    "typescript": "^4.9.5"
  }
}
```

## Available Scripts

In the root directory:
- `npm run dev`: Starts the backend server in development mode
- `npm start`: Starts the backend server in production mode
- `npm run seed`: Runs the database seeder (if available)

In the client directory:
- `npm start`: Starts the frontend development server
- `npm build`: Builds the frontend for production
- `npm test`: Runs frontend tests
- `npm run eject`: Ejects from Create React App

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details 