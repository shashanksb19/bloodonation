# Blood Donation Management System

A web application to connect blood donors with those in need of blood donations. This system facilitates blood donation requests, donor matching, and managing the donation process.

## Features

- User Authentication (Donors, Recipients, Admins)
- Blood Donation Request Management
- Donor Search and Matching
- Real-time Status Updates
- User Profile Management
- Blood Type Matching System

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (v4 or higher)
- npm or yarn package manager

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd bloodonation
```

2. Install dependencies:
```bash
npm install
```

3. Create a .env file in the root directory with the following content:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/bloodonation
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
```

4. Start MongoDB service on your machine

5. Start the server:
```bash
npm start
```

The server will start running on http://localhost:5000

## API Endpoints

### User Routes
- POST /api/users/register - Register a new user
- POST /api/users/login - Login user
- GET /api/users/profile - Get user profile
- PATCH /api/users/profile - Update user profile
- GET /api/users/donors - Get all donors
- GET /api/users/donors/search - Search donors by blood type

### Blood Request Routes
- POST /api/blood-requests - Create new blood request
- GET /api/blood-requests - Get all blood requests
- GET /api/blood-requests/user - Get user's blood requests
- PATCH /api/blood-requests/:id/status - Update request status
- POST /api/blood-requests/:id/match - Match donor to request
- PATCH /api/blood-requests/:requestId/donor-response - Update donor response

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License. 