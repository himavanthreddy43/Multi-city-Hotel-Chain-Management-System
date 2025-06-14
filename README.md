# 🏨 Multi-city Hotel Chain Management System

This project is a **relational database design and implementation** for managing operations across a multi-city hotel chain. Developed using **MySQL**, it focuses on effectively handling hotel branches, rooms, guest bookings, employee details, and feedback systems.

## 📌 Features

- **Hotel Management**: Tracks hotel branches by city, star rating, manager, and room capacity.
- **Room Management**: Maintains availability, room type, and pricing per hotel.
- **Guest Management**: Stores guest details, loyalty level, and booking history.
- **Employee Management**: Assigns employees to hotels with shift and role tracking.
- **Booking System**: Manages room reservations, check-in/check-out, and billing.
- **Feedback & Loyalty**: Links guest feedback to bookings, affecting loyalty status.

## 🗃️ Database Schema Overview

### 1. `Hotel`
- hotel_code *(Primary Key)*
- name, city, manager_id, number_of_rooms, star_rating

### 2. `Room`
- room_id *(Primary Key)* (Auto-increment)
- room_number (Unique per hotel), type, price_per_night, availability_status
- Foreign key: `hotel_code → Hotel`

### 3. `Guest`
- guest_id *(Primary Key)* (Auto-increment)
- name, loyalty_level *(Silver / Gold / Platinum)*

### 4. `Employee`
- employee_id *(Primary Key)*
- name, role, hotel_code, shift_details
- Foreign key: `hotel_code → Hotel`

### 5. `Booking`
- booking_id *(Primary Key)* (Auto-increment)
- guest_id, room_id, check_in_date, check_out_date, total_bill
- Foreign keys: `guest_id → Guest`, `room_id → Room`

### 6. `Feedback`
- feedback_id *(Primary Key)* (Auto-increment)
- booking_id *(One-to-One)*, guest_id, rating *(1-5)*, comments
- Foreign keys: `booking_id → Booking`, `guest_id → Guest`

## 📥 Sample Data

The project includes pre-populated records for:
- Hotels in Goa, Manali, and Delhi
- Multiple room types and availability
- Registered guests with different loyalty levels
- Managers and employees across different shifts
- Bookings and associated feedback entries

## 💡 Learning Outcomes

- Learned to design normalized relational schemas
- Used `FOREIGN KEY`, `UNIQUE`, `CHECK`, and `ENUM` constraints
- Implemented one-to-many and one-to-one relationships
- Applied integrity constraints and business rules in SQL

## 🛠️ Tools Used

- MySQL Workbench / Command Line
- ER Diagram (designed manually or via tool)
- Git & GitHub for version control and publishing

![WhatsApp Image 2025-06-14 at 14 24 18_b23ce43c](https://github.com/user-attachments/assets/b27bad95-7600-48f6-819f-c4283875054d)


![WhatsApp Image 2025-06-14 at 14 36 11_20a73000](https://github.com/user-attachments/assets/f72db642-4f8c-4428-888b-6932d5aebc8a)

