# Online Food Ordering and Restaurant Management System

This repository contains the complete source code for the "Online Food Ordering and Restaurant Management System" built using the PERN stack (PostgreSQL, Express, React, Node.js).

## System Architecture
- **Frontend**: React.js (via Vite) + Tailwind CSS
- **Backend**: Node.js + Express.js
- **Database**: PostgreSQL (managed via Prisma ORM)

---

## Hardware Requirements
To run this project locally or on a production server, the following minimum hardware specifications are recommended:
- **Processor**: Intel Core i3 (7th Gen or above) / AMD Ryzen 3 or equivalent.
- **RAM**: Minimum 4 GB (8 GB recommended for smooth concurrent development).
- **Storage**: Minimum 2 GB of free disk space (SSD preferred for faster read/write operations).
- **Network**: A stable internet connection (for downloading NPM packages and external API interactions if any).

## Software Requirements
The following software tools and runtimes must be installed on your system to run the project:
1. **Operating System**: Windows 10/11, macOS (Catalina or newer), or any standard Linux distribution (Ubuntu 20.04+).
2. **Node.js**: Version 18.x or higher (LTS recommended).
3. **NPM**: Node Package Manager (comes bundled with Node.js).
4. **PostgreSQL**: Version 14.x or higher (or SQLite for local lightweight testing).
5. **Git**: For version control.
6. **Code Editor**: Visual Studio Code (VS Code) is highly recommended.

---

## Installation & Setup Guide

### 1. Backend Setup
1. Open a terminal and navigate to the `backend` directory:
   ```bash
   cd backend
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Set up the Environment Variables:
   Create a `.env` file in the `backend` directory and add the following:
   ```env
   DATABASE_URL="file:./dev.db" # Change to PostgreSQL URL for production
   JWT_SECRET="your_super_secret_key"
   PORT=5000
   ```
4. Initialize the Database:
   ```bash
   npx prisma generate
   npx prisma db push
   ```
5. Start the backend server:
   ```bash
   npm run dev
   ```

### 2. Frontend Setup
1. Open a new terminal and navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Set up Environment Variables:
   Create a `.env` file in the `frontend` directory:
   ```env
   VITE_API_URL="http://localhost:5000/api"
   ```
4. Start the frontend development server:
   ```bash
   npm run dev
   ```

---

## Project Structure Highlights
- `/backend/prisma`: Database models and ORM configurations.
- `/backend/src/routes`: Express endpoints for Auth, Orders, and Restaurants.
- `/backend/src/middleware`: JWT authentication and RBAC control.
- `/frontend/src/pages`: React pages (Home, Menu, Dashboard, Checkout).
- `/frontend/src/context`: Global state management for User Authentication and Cart logic.
