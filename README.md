# SplitEasy

**SplitEasy** is a web application built using the **MERN stack** (MongoDB, Express, React, Node.js) to help users share and manage expenses with friends and family in an efficient, transparent manner.

## Table of Contents
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Project Structure](#project-structure)
- [API Documentation](#api-documentation)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## Key Features
- **Create and Share Groups**: Create groups, add members, and manage expenses within the group.
- **Expense Tracking**: Easily add and track shared expenses. Split expenses equally, by exact amounts, or by percentages.
- **Automatic Share Calculation**: Automatically calculates how much each group member owes or is owed.
- **View Group Balances**: View the total balance of each member in the group and their outstanding amount.
- **Settle Up**: Members can settle up their balances directly through the app.

## Tech Stack

- **Front-end**: [ReactJS](https://reactjs.org/)
- **Back-end**: [ExpressJS](https://expressjs.com/) and [NodeJS](https://nodejs.org/)
- **Database**: [MongoDB](https://www.mongodb.com/)

## Getting Started

### Prerequisites

To run this project, you'll need the following installed on your machine:

- [Node.js](https://nodejs.org/) (version 14 or above)
- [MongoDB](https://www.mongodb.com/) (local or cloud instance)
- A code editor like [VSCode](https://code.visualstudio.com/)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SplitEasy.git
   cd SplitEasy
Install dependencies for both the front-end and back-end.

Front-end:
bash
Copy code
cd client
npm install
Back-end:
bash
Copy code
cd ../server
npm install
Set up environment variables:

Create a .env file in the server directory and add the following:

env
Copy code
PORT=5000
MONGO_URI=<your_mongoDB_connection_string>
JWT_SECRET=<your_secret_key>
Ensure that you replace <your_mongoDB_connection_string> with your actual MongoDB connection URL and <your_secret_key> with a secret string for JWT authentication.

Running the App
Start the MongoDB server (if running locally):

bash
Copy code
mongod
Run the back-end server:

bash
Copy code
cd server
npm start
Run the front-end development server:

bash
Copy code
cd ../client
npm start
Open your browser and go to http://localhost:3000 to see the app running!

Project Structure
bash
Copy code
SplitEasy/
│
├── client/                 # Front-end (React) source files
│   ├── public/             # Static assets
│   └── src/                # React components, pages, and services
│       ├── components/     # Reusable components like forms, buttons, etc.
│       ├── pages/          # React pages (Dashboard, Group, etc.)
│       └── services/       # API services
│
├── server/                 # Back-end (Node/Express) source files
│   ├── config/             # Database and server configurations
│   ├── controllers/        # Request handlers for API endpoints
│   ├── models/             # Mongoose models for MongoDB
│   ├── routes/             # API routes
│   └── middleware/         # Middleware for authentication, validation, etc.
│
└── README.md               # Project documentation
API Documentation
Authentication
POST /api/auth/register: Register a new user.
POST /api/auth/login: Login to an existing account.
Group Management
POST /api/groups: Create a new group.
GET /api/groups: Fetch all groups for the logged-in user.
POST /api/groups/:groupId/expense: Add an expense to a specific group.
Expense Management
POST /api/expenses: Add a new expense.
GET /api/expenses: Get all expenses for the logged-in user.
Settlement
POST /api/groups/:groupId/settle: Settle balances within a group.
For more detailed API usage, check out the Postman collection.

Future Enhancements
Payment Integration: Settle balances via online payment methods.
Notifications: Email or SMS notifications for members to settle up.
Expense Categories: Categorize expenses (e.g., food, travel, etc.) for better insights.
Multi-currency Support: Add support for managing expenses in different currencies.



