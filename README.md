# Hotel_Room_Reservation_System
# 🏨 Hotel Room Reservation System

A web-based **Hotel Room Reservation System** built with React.  
Implements an **optimal room booking algorithm** that minimizes guest travel time within the hotel, based on horizontal (room-to-room) and vertical (floor-to-floor) distances.  

---

## 📌 Problem Statement
The hotel has **97 rooms** distributed across **10 floors**:
- **Floors 1–9** → 10 rooms each (e.g., 101–110, 201–210, …).
- **Floor 10** → 7 rooms only (1001–1007).
- Stairs/Lift are on the **left side**, and rooms are ordered left → right.

### Travel Time Rules
- **Horizontal**: moving between adjacent rooms = 1 minute.
- **Vertical**: moving between floors = 2 minutes per floor.

### Booking Rules
1. A single guest can book up to **5 rooms**.
2. Priority is to book on the **same floor** if possible.
3. If not, the system assigns rooms that **minimize total travel time** (horizontal + vertical).
4. Contiguous rooms near the **stairs/lift** are preferred in tie cases.

---

## 🚀 Features
- Enter the number of rooms (1–5) to book.
- **Optimal assignment** of rooms based on availability.
- Visualization of the hotel building:
  - 🟩 Free rooms  
  - 🟥 Occupied rooms  
  - 🟦 Booked rooms (this session)  
  - ⬜ Stairs/Lift
- Buttons:
  - **Generate Random Occupancy** → simulate availability.
  - **Reset All** → clear bookings and reset hotel state.
- Displays **total travel time** (with breakdown).

---

## 🛠️ Tech Stack
- **Frontend**: React (with TailwindCSS for UI)
- **Deployment**: Works on Vercel, Localhost, or Google Colab (with localtunnel/cloudflared for live demo).

---

## ▶️ Running Locally
1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/hotel-reservation.git
   cd hotel-reservation
