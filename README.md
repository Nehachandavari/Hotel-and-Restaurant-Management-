# Hotel-and-Restaurant-Management

This code implements a basic Hotel Management System in C++. It defines multiple classes to manage guests, rooms, employees, restaurant services, reservations, and billing.

## Classes and Their Purpose

### 1. Restaurant Class:
- Manages the menu and takes orders from guests.
- Adds GST to the total bill.

### 2. Guest Class:
- Stores guest details like name and Aadhaar number, validating the number to ensure it’s 12 digits.

### 3. Room Class (and Derived Classes):
- **Room**: A base class that contains room attributes like room number, price, availability, features, and room type.
- **SingleRoom**, **DoubleRoom**: Derived classes with specific features.
- Manages room services such as housekeeping, laundry, and restaurant services.

### 4. Employee Class (and Derived Classes):
- **Employee**: A base class that defines employee attributes and their work.
- **Receptionist**, **Housekeeping**, **Manager**, **Bellboy**, **Chef**: Derived classes with different work roles.

### 5. Reservation Class:
- Manages reservations by linking a guest to a room with a duration.

### 6. Bill Class:
- Stores billing details and payment status for reservations.

### 7. Hotel Class:
- Manages the hotel’s rooms, reservations, employees, and bills.
- Handles room booking, checkout, and displaying available rooms and employees.

## Key Features of the Code
- **Display of Room Features**: Shows special features based on room types (Single, Double).
- **Service Request Options**: Allows users to request housekeeping, laundry, or restaurant services.
- **Aadhaar Validation**: Throws an error if the entered Aadhaar number isn't 12 digits.
- **Booking and Checkout System**: Implements a booking system for guests and tracks billing with payment status.
- **Employee Management**: Adds and displays different employees along with their responsibilities.

## Functionality Overview

### 1. Hotel Structure and Rooms:
- The `Hotel` class maintains a list of rooms (`SingleRoom`, `DoubleRoom`) with different features, pricing, and availability status.
- It allows the addition and tracking of up to 8 rooms with information on their features and types.
- The `Hotel` class includes a method to display available rooms, showcasing their type, price, and special features.

### 2. Guest and Employee Management:
- The `Guest` class manages guest information, including the guest's name and 12-digit Aadhar number, which is validated.
- The `Employee` class defines different types of employees (`Receptionist`, `Housekeeping`, `Manager`, `Bellboy`, `Chef`) and their roles using a virtual work method.

### 3. Restaurant Services:
- The `Restaurant` class contains a simple menu with prices and methods to take orders from guests. It calculates the total bill, including GST.
- Guests can order from the restaurant during their stay, and this can be requested through the room service menu.

### 4. Room Reservations and Billing:
- The `Hotel` class allows booking and checking out of rooms for guests, assigning each guest a reservation and generating a bill.
- Room reservation includes checking room availability, storing the reservation details, and assigning a guest to a specific room for a specified duration.
- Upon checkout, the system calculates the bill based on room pricing and the number of days stayed.

### 5. Room Features and Services:
- Each room type (`SingleRoom`, `DoubleRoom`) comes with specific features such as AC, TV which are displayed when viewing room details.
- Guests can request additional services like housekeeping, laundry, or restaurant services through the `Room` class.

### 6. Bill Generation and Payment:
- Bills are generated based on room price and duration of stay, and a bill is marked as paid upon successful checkout.
- The `Bill` class tracks total amount and payment status.


