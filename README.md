# Task-Manager-Core
Task Management API with MongoDB
Project Overview
Project Title
Task Management API with User Authentication
Project Description
This project is a backend RESTful API built using Node.js, Express.js, and MongoDB. It allows users to register, log in securely, and manage their personal tasks. Each task is associated with a specific user, ensuring data privacy and secure access.
Project Goals & Objectives
•	Understand NoSQL databases and MongoDB
•	Implement database integration using Mongoose
•	Design schemas and relationships
•	Build secure user authentication using JWT
•	Perform full CRUD operations
•	Apply pagination, filtering, and sorting
•	Follow industry-level backend architecture
________________________________________
System Architecture
Architecture Overview
The application follows a Layered MVC Architecture:
•	Client (Postman / Frontend) → Sends HTTP requests
•	Routes Layer → Handles API endpoints
•	Controller Layer → Business logic
•	Model Layer → MongoDB schemas using Mongoose
•	Database Layer → MongoDB Atlas (Cloud)
Architecture Flow
Client → Routes → Controllers → Models → MongoDB Atlas
________________________________________
Technology Stack
•	Backend Runtime: Node.js
•	Framework: Express.js
•	Database: MongoDB Atlas (NoSQL)
•	ODM: Mongoose
•	Authentication: JWT (JSON Web Token)
•	Password Security: bcryptjs
•	Testing Tool: Postman
•	Deployment Platforms: Render / Railway / Cyclic
________________________________________
Setup Instructions
Prerequisites
•	Node.js installed
•	MongoDB Atlas account
•	Git installed
•	Postman installed
Step-by-Step Installation
1.	Clone the repository
git clone <repository-url>
cd task-manager-api
2.	Install dependencies
npm install
3.	Create environment file
        PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_secret_key
    4.Start the server
npm run dev
5.Server will run on:
http://localhost:5000

Code Structure
task-manager-api/
│── server.js
│── package.json
│── .env.example
└── src/
├── config/
│ └── database.js
├── models/
│ ├── User.js
│ └── Task.js
├── controllers/
│ ├── userController.js
│ └── taskController.js
├── middleware/
│ └── auth.js
└── routes/
├── userRoutes.js
└── taskRoutes.js
Database Design & Relationships
User Collection
•	name (String)
•	email (String, unique)
•	password (Hashed)
Task Collection
•	title (String)
•	description (String)
•	completed (Boolean)
•	priority (Enum)
•	user (ObjectId – reference to User)
Relationship
•	One-to-Many
•	One User → Multiple Tasks
________________________________________
API Features
Authentication
•	User Registration
•	User Login
•	JWT-based protected routes
Task Management
•	Create Task
•	Read Tasks (pagination & filtering)
•	Update Task
•	Delete Task
Advanced Features
•	Pagination using limit & page
•	Filtering by completion status
•	Sorting by creation date
•	Secure user-based data access
________________________________________
Technical Details
Algorithms Used
•	Password hashing using bcrypt (salt rounds)
•	JWT token generation and verification
•	MongoDB query optimization using indexes
Data Structures
•	JSON objects for API communication
•	MongoDB documents for data storage
•	Arrays for task lists
________________________________________
Testing Strategy
Manual Testing
•	Tested all APIs using Postman
•	Verified authentication tokens
•	Checked CRUD operations
•	Tested invalid inputs and error handling
Sample Test Cases
•	Register user with valid data
•	Login with correct credentials
•	Access protected route without token (Fail)
•	Create task with valid token (Success)
Visual Documentation
Screenshots Included
•	User Login (Token received)


 
 
•	Create Task API response



 

 
 

 

 
Deployment Process
1.	Push project to GitHub
2.	Create account on Render / Railway
3.	Connect GitHub repository
4.	Add environment variables
5.	Deploy backend
