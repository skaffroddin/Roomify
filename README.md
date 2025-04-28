# Hotel Room Booking Website

## Objective
To build a hotel room booking platform where users can:
- View available rooms
- Book and cancel rooms
- See their bookings
- Allow admins to manage rooms

---

## Tech Stack
- **Laravel** (Latest stable version)
- **JavaScript & AJAX**
- **Blade Templates**
- **MySQL or SQLite** (Relational Database)

---

## Features

### 1. Authentication
- Basic login/register system for users.

### 2. Room Management (Admin)
- Admin can:
  - Perform CRUD operations for rooms:
    - Room Number
    - Room Type
    - Price
    - Status (Available/Booked)
  - View the room list with AJAX-based filtering and search.

### 3. Booking Module (User)
- Users can:
  - View available rooms.
  - Book a room in real-time using AJAX.
  - Cancel their bookings.
  - Booking updates room status to **Booked**.

### 4. Cancel Booking
- Cancelling a booking updates the room status to **Available**.

### 5. Date Range Booking
- **Features:**
  - Add a date range picker for check-in and check-out dates.
  - Prevent overlapping bookings:
    - A room cannot be booked for a date range overlapping with an existing booking.
    - For example, a room booked from April 10–12 cannot be booked from April 11–13.
  - Highlight unavailable dates dynamically in the calendar.
  - Ensure bookings cannot be made in the past.
  - Use AJAX to check room availability in real-time as the user selects dates.

### 6. Conflict Detection
- Backend validation to ensure booking overlaps are prevented.
- Highlight unavailable dates dynamically in the calendar UI.
- Optionally display a list of fully-booked dates for each room.
- Show real-time availability using AJAX.

### 7. Live Search with Filters
- AJAX-based live search functionality including:
  - **Debounced Input**: Reduces server load by delaying the request until the user stops typing.
  - Filters for:
    - Room Type
    - Price Range
    - Date Availability
  - Combine multiple filters efficiently.

### 8. Admin Dashboard with Booking Stats
- Display booking statistics such as:
  - Booking trends.
  - Most booked room type.
  - Upcoming vs. past bookings.
  - Total rooms and bookings.
- Use visualization tools like **Chart.js** or similar.

---

## Performance Optimizations
- Server-side pagination to handle large datasets efficiently.
- Eloquent eager loading to avoid the **N+1 Query Problem**.
- User-friendly AJAX loaders and toasts for better feedback.

---

## Evaluation Criteria
| Area                       | Weight |
|----------------------------|--------|
| **Code Structure & Cleanliness** | 20%    |
| **Laravel Best Practices**       | 20%    |
| **AJAX Integration**             | 20%    |
| **Functional Coverage**          | 20%    |
| **UI/UX & Feedback**             | 10%    |
| **Bonus/Advanced Features**      | 10%    |

---

## Installation Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-repo/hotel-booking.git
   cd hotel-booking
   ```

2. **Install Dependencies**
   ```bash
   composer install
   npm install
   ```

3. **Setup Environment Variables**
   - Copy `.env.example` to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Update `.env` with database credentials and other configurations.

4. **Generate Application Key**
   ```bash
   php artisan key:generate
   ```

5. **Run Migrations**
   ```bash
   php artisan migrate
   ```

6. **Seed the Database** (Optional: Add dummy data for testing)
   ```bash
   php artisan db:seed
   ```

7. **Run the Development Server**
   ```bash
   php artisan serve
   ```

8. **Compile Frontend Assets**
   ```bash
   npm run dev
   ```

---

## Project Structure
- **Authentication**: Laravel’s default authentication system with customizations.
- **Database Models**:
  - `User`: For storing user information.
  - `Room`: For storing room details.
  - `Booking`: For storing booking information.
- **AJAX**: Used for real-time updates in features like booking, filtering, and search.
- **Blade Templates**: For creating responsive and dynamic pages.

---

## Key Dependencies
- Laravel (latest stable version)
- MySQL/SQLite (Relational Database)
- Chart.js (Admin Dashboard)
- Date Range Picker Library
- Laravel Breeze or Fortify (Authentication)

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgements
- Laravel documentation
- Chart.js library
- Date Range Picker library
- Open-source contributors

---

For questions or feedback, please contact [Your Name] at [Your Email].

