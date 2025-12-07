# Vehicle Rental System

**Live Deployment:** https://rental-system-rust.vercel.app/

##  Project Overview

A backend API for a vehicle rental management system that handles:
- **Vehicles** - Manage vehicle inventory with availability tracking
- **Customers** - Manage customer accounts and profiles
- **Bookings** - Handle vehicle rentals, returns and cost calculation
- **Authentication** - Secure role-based access control (Admin and Customer roles)

##  Technology Stack

- **Node.js** + **TypeScript**
- **Express.js** (web framework)
- **PostgreSQL** (database)
- **bcrypt** (password hashing)
- **jsonwebtoken** (JWT authentication)

##  Features

###  Authentication & Roles
- JWT-based signin
- Password hashing with bcrypt
- Role based autorization
    - `Admin` -> Full access
    - `Customer` -> Can register, browse vehicles and can manage their own bookings

###  Vehicle Management
- `Add`, `Update`, `Delete` vehicles (Admin only)
- Public endpoints for browsing single or all vehicles

###  User Management
- `Browse`, `Update`, `Delete` users (Admin only)
- Customers can manage their own profile
- Safe deletaion (Users cannot be deleted if they have active bookings)

###  Booking Management
- Create bookings with vehicle availability validation
- Auto Update vehicle status (booked/available)
- Browse all bookings (Admin only)
- Customers can brose their own bookings
- Cancel or Return bookings based on role and rules


