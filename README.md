# Intern Management System - Backend

## Overview
This repository contains the backend services for the Intern Management System. It handles core functionalities such as user authentication, task management, attendance tracking, report generation, and admin functionalities.

## Features

### Authentication & Authorization
- User login and logout functionality.
- Role-based access control for Admins, Managers, and Interns.

### Task Management
- API for creating, assigning, updating, and deleting tasks.
- Categorization of tasks for better organization.

### Account Management
- Automatic account deletion for interns after internship completion.

### Attendance Management
- APIs for tracking and managing intern attendance.

### Report Generation
- Generate and download reports in Excel and PDF formats via API.

### Roles & Permissions
- Role-based APIs for Admin and Manager functionalities.

### Chatbot Integration (Low Priority)
- Basic chatbot endpoints for limited conversational functionality.

## Tech Stack
- **Programming Language**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB
- **Authentication**: JWT-based authentication or session management

## Setup and Installation

### Clone the repository:
```bash
git clone https://github.com/Ashishpatel011/iisppr-intern-management-backend.git
cd intern-management-backend
```

### Install dependencies:
```bash
npm install  # For Node.js
# OR
pip install -r requirements.txt  # For Python
```

### Configure environment variables:
Create a `.env` file in the root directory and set the following variables:
```env
MONGO_URI=mongodb+srv://iamashish761:ashish761@cluster0.55exu.mongodb.net/ims_db
JWT_SECRET=your_secret_key
```

### Run database migrations (if applicable):
```bash
npm run migrate  # Node.js example
# OR
flask db upgrade  # Python example
```

### Start the development server:
```bash
npm run dev  # For Node.js
# OR
python app.py  # For Python
```

### Access the API:
The backend server will run on `http://localhost:<port>`.

## API Endpoints

### Authentication
- **POST** `/auth/login` - Login for users.
- **POST** `/auth/logout` - Logout for users.

### Task Management
- **POST** `/tasks` - Create a new task.
- **GET** `/tasks` - Retrieve all tasks.
- **PUT** `/tasks/:id` - Update task details.
- **DELETE** `/tasks/:id` - Delete a task.

### Attendance
- **POST** `/attendance` - Mark attendance.
- **GET** `/attendance` - Retrieve attendance records.

### Reports
- **GET** `/reports?format=excel|pdf` - Generate reports.

### Account Management
- **DELETE** `/users/:id` - Auto-delete user accounts post internship.
