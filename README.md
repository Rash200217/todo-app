# Creative Todo Web App 🎨

A modern, fast, and beautiful task management application built with **Laravel 12** (Backend) and **React + Vite** (Frontend).
It features a stunning **Glassmorphism UI**, role-based access control (Admin/User), and powerful task organization tools.

![Project Status](https://img.shields.io/badge/status-active-success.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 🚀 Features

### Core Features
- **Task Management**: Create, Read, Update, and Delete (CRUD) tasks.
- **Scheduling**: Add Due Dates and Times to tasks (⏰).
- **Edit Tasks**: Update task details, dates, and times easily via a modal.

### ✨ New Features
- **Categories & Tags** 🎨: Organize tasks with color-coded tags (e.g., Work, Personal).
- **Search & Filters** 🔍: Find tasks instantly by title, status, or category.
- **In-App Notifications** 🔔: Get alerts for tasks due within the next 24 hours.

### for Admins
- **User Management**: View all registered users and their task counts.
- **User Deletion**: Delete users (and their data) directly from the dashboard.
- **Task Oversight**: View and manage tasks for any specific user.

## 🛠 Tech Stack

- **Frontend**: React.js, TailwindCSS, Vite, Axios, React-Calendar.
- **Backend**: Laravel 12 API, Sanctum (Auth), MySQL.
- **Design**: Custom CSS, Glassmorphism effects, Responsive Grid Layouts.

## ⚙️ Installation & Setup

### Prerequisites
- PHP 8.2+
- Composer
- Node.js & NPM
- MySQL Database

### 1. Backend Setup (Laravel)
***First you need to create a database named "todo_db" in phpmyadmin.***
```bash
cd backend

# Install PHP dependencies
composer install

# Set up environment file
cp .env.example .env
# Configure your DB_ connections in .env

# Generate App Key
php artisan key:generate

# Run Migrations (creates tables for tasks, categories, notifications)
php artisan migrate

# Start the Scheduler (for Notifications)
php artisan schedule:work

# Start the Server
php artisan serve
```
*The backend will run at `http://127.0.0.1:8000`*

### 2. Frontend Setup (React)

```bash
cd frontend

# Install Node dependencies
npm install

# Start the Content
npm run dev
```
*The frontend will run at `http://localhost:5173` (or similar)*

## 🔑 Usage

### Creating an Admin
The system automatically assigns **Admin** privileges if the user's **Name** begins with `admin` (case-insensitive).

### Notifications
To test notifications manually without waiting for the scheduler:
```bash
php artisan app:check-due-tasks
```

## 📸 Screenshots

![Image](https://github.com/user-attachments/assets/7cbda870-11c7-48ed-ae39-66e0e0c8ccc3)
![Image](https://github.com/user-attachments/assets/4eacc5f1-7171-44fd-a881-e51e01ea0385)
![Image](https://github.com/user-attachments/assets/14a1a3d8-a449-4764-bf4a-4b80c4ce47b9)
![Image](https://github.com/user-attachments/assets/7203ab5e-94d3-45ce-91eb-ebf44acb0356)

## 📝 License
This project is open-source and available under the MIT License.

---
Made By *Rashmika Dhananjaya*
