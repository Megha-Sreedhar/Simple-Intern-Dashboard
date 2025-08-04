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
2. Define **`ADMIN_USERNAME`** and **`REACT_APP_BACKEND_URL`** in `/frontend/.env`.
3. Run the **Admin Seeder Script**:

   ```bash
   cd backend
   node seedAdmin.js
   ```

   - Creates admin if not exists.
   - Updates password if admin exists but password differs.

4. Access **Admin Panel** at:

   ```
   /admin/login
   ```

   (Credentials are secured via `.env`)

## How to Run Locally

```bash
# Clone the repository
git clone https://github.com/Megha-Sreedhar/Simple-Intern-Dashboard.git
cd SimpleInternDashboard

# Backend Setup
cd backend
npm install
# Add .env file and run:
node seedAdmin.js
npm start

# Frontend Setup
cd ../frontend
npm install
# Add .env file
npm start
```

## Key Functional Modules

### Intern/User Module:

- Registration with referral code.(Try This SW9D8B)
- Dashboard displaying referral code, earnings, leaderboard rank.
- Change Password & Forgot/Reset Password.
- Contact Us Form with dynamic fields.
- If Sometimes Deployed Not Work Then Try Locally Please

### Admin Module:

- Admin Login (Environment-based Credentials).
- User Management (View, Delete, Update Funding).
- Contact Message Management.
- Password Change functionality.

### Referral & Funding Logic:

- Every new referral increments the referrer's total funding by ₹500.
- Leaderboard dynamically ranks based on total raised funds.

## To-Do (Enhancements Roadmap)

- SMTP Email Integration for Forgot/Reset Password.
- Pagination & Filtering in Admin Panels.
- Enhanced UI for mobile devices.
- Advanced analytics on dashboard.

## Submission Notes

This project fulfills the Round 1 requirements:
- Dummy login/signup 
- Dashboard with intern name, referral code, donations, rewards 
- Simple backend API returning dummy data 
- Bonus leaderboard 



