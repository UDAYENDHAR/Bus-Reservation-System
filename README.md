# 🚌 Bus Reservation System  

A simple and functional console-based **Bus Reservation System** built using **Java**.  
It follows a clean modular architecture with DAO classes for easy maintenance, scalability, and clean data handling.

---

## 📌 Features

- Add buses with number, capacity, and type  
- Display all available buses  
- Book seats with passenger details  
- Prevent double booking using seat availability validation  
- Modular DAO structure for clean separation of logic  
- Optional database support via `DbConnection.java`  

---

## 🧩 System Architecture

User (Console)
     │
     ▼
BusDemo.java (Main Runner)
     │
     ├── BusDAO.java       → Bus operations
     ├── BookingDAO.java   → Booking operations
     │
     ▼
Database (via DbConnection.java)
---

## 📁 Project Structure

/BusReservationSystem
│
├── Bus.java
├── BusDAO.java
├── Booking.java
├── BookingDAO.java
├── DbConnection.java
└── BusDemo.java
---

### **Class Descriptions**

| Class | Responsibility |
|-------|----------------|
| `Bus` | Data model for Bus (bus number, capacity, AC info, etc.) |
| `BusDAO` | Handles loading, saving, and displaying bus records |
| `Booking` | Data model for booking (name, age, date, bus number) |
| `BookingDAO` | Handles booking validation and seat availability |
| `DbConnection` | Manages database connection (if DB is used) |
| `BusDemo` | Console UI and main program runner |

---

## 🚀 How the System Works

1. User runs `BusDemo`
2. Menu options appear:
   - Add Bus  
   - View Buses  
   - Book Ticket  
3. Booking flow:
   - Checks if bus exists  
   - Checks remaining seats  
   - Adds booking only if valid  

---

## 🧪 Sample Console Output

Add Bus

View Buses

Book Ticket

Exit

Enter choice: 3
Enter Passenger Name: Rahul
Enter Age: 21
Enter Bus Number: 101
Enter Journey Date (dd-MM-yyyy): 05-12-2025

Booking Successful!



---

## 🛠️ Requirements

- Java 8+  
- Optional: MySQL or other DB (depending on your DbConnection setup)

---

## ▶️ How to Run

```bash
# Compile all files
javac *.java

# Run main program
java BusDemo

```




