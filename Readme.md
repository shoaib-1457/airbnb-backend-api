# 🏨 Airbnb Backend API

A backend API for a hotel management and booking platform inspired by Airbnb.  
This system supports hotel onboarding, room and inventory management, booking flow, payments, and secure user authentication.

---

## 📌 Overview

The Airbnb Backend API is designed to handle the complete lifecycle of hotel bookings.  
It provides RESTful APIs for **admins**, **users**, and **guests**, ensuring scalability, security, and clean separation of responsibilities.

---

## 🚀 Features

### 🔐 User Authentication
- User signup and login
- JWT-based access and refresh tokens

### 🏨 Hotel Management (Admin)
- Create, update, activate, and delete hotels
- Retrieve all hotels managed by an admin

### 🛏️ Room Management (Admin)
- Create, update, retrieve, and delete rooms
- Associate rooms with hotels

### 📦 Inventory Management (Admin)
- Retrieve room inventory
- Update room availability and inventory details

### 🔎 Hotel Browsing (User)
- Search hotels with filters
- View hotel and room details

### 📅 Booking Flow
- Initialize bookings
- Add guests to a booking
- Cancel bookings
- Track booking status
- Generate booking reports

### 👥 Guest Management
- Add, update, fetch, and delete guests linked to a user

### 💳 Payments
- Initiate booking payments
- Capture payment confirmations using webhooks

---

## 🧩 API Endpoints

### 🔐 Authentication
```
POST   /auth/signup
POST   /auth/login
POST   /auth/refresh
```

### 👤 User Profile
```
GET    /users/profile
PATCH  /users/profile
GET    /users/myBookings
```

### 👥 Guest Management
```
GET    /users/guests
POST   /users/guests
PUT    /users/guests/{guestId}
DELETE /users/guests/{guestId}
```

### 🏨 Hotel Browsing
```
GET    /hotels/search
GET    /hotels/{hotelId}/info
```

### 📅 Booking Flow
```
POST   /bookings/init
GET    /bookings/{bookingId}/status
POST   /bookings/{bookingId}/addGuests
POST   /bookings/{bookingId}/cancel
POST   /bookings/{bookingId}/payments
```

### 📊 Reports (Admin)
```
GET    /admin/hotels/{hotelId}/bookings
GET    /admin/hotels/{hotelId}/reports
```

### 🏨 Hotel Management (Admin)
```
POST   /admin/hotels
GET    /admin/hotels
GET    /admin/hotels/{hotelId}
PUT    /admin/hotels/{hotelId}
PATCH  /admin/hotels/{hotelId}/activate
DELETE /admin/hotels/{hotelId}
```

### 🛏️ Room Management (Admin)
```
POST   /admin/hotels/{hotelId}/rooms
GET    /admin/hotels/{hotelId}/rooms
GET    /admin/hotels/{hotelId}/rooms/{roomId}
PUT    /admin/hotels/{hotelId}/rooms/{roomId}
DELETE /admin/hotels/{hotelId}/rooms/{roomId}
```

### 📦 Inventory Management (Admin)
```
GET    /admin/inventory/rooms/{roomId}
PATCH  /admin/inventory/rooms/{roomId}
```

### 🔔 Webhook
```
POST   /webhook/payment
```

---

## 🗄️ Database Schema

The system uses a relational database with entities such as:
- Users and Guests
- Hotels and Rooms
- Inventory
- Bookings
- Payments

Refer to the schema diagram included in the repository for details.

---

## 🛠️ Tech Stack

- Backend: Node.js / Java / Python
- Database: MySQL / PostgreSQL
- Authentication: JWT
- Architecture: REST APIs

---

## 📌 Status

🚧 Work in progress. More features and optimizations will be added.

---

## 📄 License

This project is intended for learning and portfolio purposes.
