# Bank Management System

## Overview

Bank Management System is a console-based banking application developed in C++ that simulates core banking operations through a role-based access model. The project demonstrates strong Object-Oriented Programming principles, efficient data management using custom data structures, and persistent storage through file handling.

The system supports account creation, account management, fund transfers, deposits, withdrawals, authentication, and transaction tracking while maintaining a modular and scalable code structure.

---

## Key Concepts Demonstrated

- Object-Oriented Programming (OOP)
- Data Structures and Algorithms
- Binary Search Tree (BST)
- Hash Table with Separate Chaining
- Linked Lists
- File Handling and Data Persistence
- Role-Based Access Control
- Modular Software Design

---

## Features

### Admin
- Create customer accounts
- Delete customer accounts
- View all registered accounts

### Staff
- Deposit funds
- Withdraw funds
- Transfer money between accounts

### Customer
- Secure login authentication
- View account details
- View transaction history

---

## Data Structures Used

| Functionality | Data Structure |
|--------------|---------------|
| Account Management | Binary Search Tree (BST) |
| User Authentication | Hash Table |
| Collision Resolution | Linked List (Separate Chaining) |

---

## Technical Highlights

- Designed a modular architecture using classes and separate modules for maintainability and scalability.
- Implemented efficient account management using a Binary Search Tree for organized account storage and retrieval.
- Utilized Hash Tables with separate chaining for fast credential lookup and authentication.
- Applied file handling to persist account and transaction data across application sessions.
- Followed Object-Oriented Programming principles including encapsulation, abstraction, inheritance, and polymorphism where applicable.
- Separated business logic, data structures, and utility functions into dedicated modules for improved code organization.

---

## Project Structure

```text
Bank-Management-System/
│
├── data/
│   └── account and transaction records
│
├── include/
│   └── header files
│
├── src/
│   ├── bst/
│   ├── hashtable/
│   ├── modules/
│   ├── utils/
│   └── main.cpp
│
├── Makefile
├── README.md
└── .gitignore
```

---

## Build and Run

### Compile

```bash
g++ -std=c++17 src/main.cpp src/bst/*.cpp src/hashtable/*.cpp src/modules/*.cpp src/utils/*.cpp -Iinclude -o bank_management_system
```

### Run

```bash
./bank_management_system
```

---

## Learning Outcomes

Through this project, I gained hands-on experience with:

- Designing applications using Object-Oriented Programming principles
- Implementing and integrating custom data structures
- Managing persistent storage using file handling
- Structuring medium-sized C++ projects using modular design
- Applying Data Structures and Algorithms to real-world scenarios

---

## Future Enhancements

- Implement AVL Trees for self-balancing account storage
- Integrate a relational database (MySQL/PostgreSQL)
- Add transaction timestamps and audit logs
- Implement Admin authentication and authorization
- Develop a graphical user interface (GUI)
- Add account search and reporting features
