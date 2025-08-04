# [Live Demo](https://simpleinterndashboard.onrender.com/) — Simple Intern Dashboard

A simple full-stack intern dashboard built for the Round 1 internship task.  
Features a dummy login/signup, dashboard with intern name, referral code, total donations raised, static rewards/unlockables, and a leaderboard.

This portal enables interns to register with referral codes, track their referral-based earnings, and allows admins to manage users, funding, and contact messages through a secured dashboard.

## Features

- **Dummy Login / Signup:** No real authentication required—allows demo access.  
- **Dashboard:**  
  - Intern name (e.g., "Megha S")  
  - Dummy referral code (e.g., `megha2025`)  
  - Total donations raised (static or returned from backend)  
  - Rewards / unlockables section (static display)  
  - Leaderboard (bonus) showing ranking with dummy data  
- **API:** Backend endpoint returns the required dashboard data.

## Tech Stack Overview

| Frontend                       | Backend             | Database      | Deployment                 |
| ------------------------------ | ------------------- | ------------- | -------------------------- |
| React.js, Tailwind CSS, AOS.js | Node.js, Express.js | MongoDB Atlas | Render (Full Stack Deploy) |
| React Toastify (Notifications) | Mongoose ORM        |               |                            |


## Environment Variables Setup

### Backend (`/backend/.env`)

```env
MONGO_URI=your_mongodb_connection_string
PORT=5000
ADMIN_USERNAME=your_admin_username
ADMIN_PASSWORD=your_admin_password
FRONTEND_URL=http://localhost:3000
```

### Frontend (`/frontend/.env`)

```env
REACT_APP_BACKEND_URL=http://localhost:5000
```

## Admin Credentials Setup Guide

1. Define **`ADMIN_USERNAME`** and **`ADMIN_PASSWORD`** in `/backend/.env` and also **`MONGO_URI`\*\***`PORT`\***\*`FRONTEND_URL`**
