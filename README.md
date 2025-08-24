# Prescripto - Full Stack Doctor Medical Appointment 

Prescripto is a full-stack web application for booking doctor appointments and managing prescriptions. It includes separate interfaces for admin, doctors, and patients.

---

## Live Links

- Frontend (Patients): https://doctor-booking-management-system-js-1.onrender.com
- Admin & Doctor Panel:https://doctor-booking-management-system-js-2.onrender.com
- Backend API:https://doctor-booking-management-system-js.onrender.com

---

## Demo Credentials

### Admin Login
- Email: navneet.889035@gmail.com  
- Password: navneet@039

### Doctor Login (access via admin panel link)
- Email: amelia@prescripto.com
- Password: amelia@123

### User/Patient Login
- Email: user@gmail.com  
- Password: user@123

> Admin and Doctor share a common panel at: https://doctor-booking-management-system-js-2.onrender.com

> Patients access the user frontend at:https://doctor-booking-management-system-js-1.onrender.com

---

## Features

- Patient, Doctor, and Admin login/signup
- JWT-based authentication and role-based routing
- Admin can manage doctors and view appointments
- Doctors can manage their availability and appointments
- Patients can view doctors and book appointments
- Razorpay integration for appointment payments
- Admin dashboard showing key metrics and recent activity

---

## Tech Stack

- Frontend: React.js
- Backend: Node.js with Express
- Database: MongoDB
- Authentication: JWT (JSON Web Tokens)
- Deployment: Render

---




## 📂 Folder Structure

├── README.md
│
├── admin # Admin & Doctor panel (React + Vite + Tailwind)
│ ├── src
│ │ ├── components # Reusable UI components (Navbar, Sidebar, etc.)
│ │ ├── context # React Contexts for global state
│ │ │ ├── AdminContext.jsx # Manages admin-related state
│ │ │ ├── DoctorContext.jsx # Manages doctor-related state
│ │ │ └── AppContext.jsx # Shared app-wide context
│ │ └── pages
│ │ ├── Admin # Admin-specific pages
│ │ │ ├── Dashboard.jsx # Admin dashboard
│ │ │ ├── AddDoctor.jsx # Form for adding doctors
│ │ │ └── Doctors.jsx # List & manage doctors
│ │ └── Doctor # Doctor-specific pages
│ │ ├── Dashboard.jsx # Doctor dashboard
│ │ ├── Profile.jsx # Doctor profile management
│ │ └── Appointments.jsx # View & manage appointments
│ └── public # Static assets (favicon, logos, etc.)
│
├── backend # Backend API (Node.js + Express + MongoDB)
│ ├── config
│ │ ├── db.js # Database connection
│ │ └── cloudinary.js # Cloudinary configuration
│ ├── controllers # Request handlers
│ │ ├── adminController.js # Admin-related APIs
│ │ ├── doctorController.js # Doctor-related APIs
│ │ └── userController.js # Patient-related APIs
│ ├── middleware
│ │ ├── authMiddleware.js # JWT authentication
│ │ └── uploadMiddleware.js # File upload handling
│ ├── models
│ │ ├── User.js # User schema (patients/admins)
│ │ ├── Doctor.js # Doctor schema
│ │ └── Appointment.js # Appointment schema
│ ├── routes
│ │ ├── adminRoutes.js # Admin API routes
│ │ ├── doctorRoutes.js # Doctor API routes
│ │ └── userRoutes.js # Patient API routes
│ └── server.js # Main Express server entry point
│
├── frontend # Patient-facing frontend (React + Vite + Tailwind)
│ ├── src
│ │ ├── components # Reusable UI (Navbar, Footer, DoctorCard, etc.)
│ │ ├── context
│ │ │ └── AppContext.jsx # Global state for patient app
│ │ └── pages
│ │ ├── Home.jsx # Homepage
│ │ ├── Doctors.jsx # Browse doctors
│ │ ├── Appointment.jsx # Book appointments
│ │ └── Profile.jsx # User profile
│ └── public # Static assets (favicon, logos, etc.)

## Notes

- Admin must approve doctors before they can receive appointments
- Doctors and admins use the same panel but have role-based views
- Patients use a separate frontend for booking and managing appointments

