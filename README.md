# RAF Cloud Manager — Angular 16 Frontend (KT1)

This project is the **frontend phase** of the RAF Cloud platform,
developed for the *Napredno Web Programiranje* course.

The goal of the application is to simulate a cloud environment where
users can create and manage virtual machines and scheduled operations.

📌 Current state (KT1):
✔ fully implemented Angular frontend  
✔ UI pages with mock data  
✔ functionality prepared for future backend integration

Backend (Spring + JWT + WebSockets) will be implemented in the next phase.

---

## 🧩 Domain Areas

The system consists of two main modules:

### 👤 Users Management

User entity contains:
- first name
- last name
- email (unique)
- password (encrypted in backend phase)
- permissions set

Client features (KT1 — mock data):

- Login page
- Users table
  - name, surname, email, permissions
- Add user form
  - all fields required
  - client-side validation
- Edit user page
  - form pre-filled with existing values

Permissions affect UI visibility (in KT2+JWT phase),
but page structure is already prepared.

---

### 🖥 Machines Management

Machine entity (base attributes):

- id
- name
- type
- description
- status (ON / OFF)
- createdBy user id
- active (soft delete flag)

Frontend features (KT1 — mock data):

- Machines search page
  - filter form (name, type, state, date range)
  - table with user-owned machines
- Create machine form
  - name only (other attributes handled by backend later)
- Errors history page
  - list of scheduled operation failures
  - shows:
    - timestamp
    - machine id
    - operation
    - error message

---

## ✨ Planned Features (backend phase)

These features will be implemented in KT2:

- Spring Boot backend
- JWT authentication & authorization
- permissions enforcement
- scheduling operations:
  - start
  - stop
  - restart
- async operations (10+ seconds delay)
- WebSocket state updates
- soft delete (destroy machine)
- error logging for failed scheduled actions

---

## 🛠 Tech Stack

Frontend:
- Angular 16
- TypeScript
- Angular Router
- Reactive Forms

State / mock data:
- in-memory structures (KT1)

Backend (planned):
- Spring Boot
- JWT
- WebSockets
- relational database

---

## ▶ Running the project
Application runs at: http://localhost:4200

---

## 👩‍💻 Author

Marija Erić  
Final-year Computer Engineering student — RAF Belgrade

Backend integration is currently in progress.


