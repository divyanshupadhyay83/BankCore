# BankCore

## Overview

BankCore is a console-based banking application developed in C++ that simulates core banking operations through a role-based access model. The project demonstrates Object-Oriented Programming principles, efficient data management using custom data structures, and persistent storage through file handling.

The system supports account management, fund transfers, deposits, withdrawals, authentication, and transaction tracking while maintaining a modular and organized code structure.

---

## Key Concepts Demonstrated

- Object-Oriented Programming (OOP)
- Data Structures and Algorithms
- Binary Search Tree (BST)
- Hash Table
- Linked Lists
- File Handling and Data Persistence
- Role-Based Access Control
- Modular Software Design

---

## Features

### Admin

- Create customer accounts
- Delete customer accounts
- View registered accounts
- Manage account-related operations

### Staff

- Deposit funds
- Withdraw funds
- Transfer money between accounts
- Access customer account information

### Customer

- Secure login authentication
- View account details
- Check account balance
- Deposit and withdraw funds
- Transfer money
- View transaction history

---

## Data Structures Used

| Functionality | Data Structure |
|---|---|
| Account Management | Binary Search Tree (BST) |
| User Authentication | Hash Table |
| Collision Resolution | Linked List / Separate Chaining |
| Account Records | Node-based Data Structures |

---

## Technical Highlights

- Designed a modular architecture using classes and separate modules for maintainability and better code organization.
- Implemented account management using a Binary Search Tree for organized account storage and retrieval.
- Utilized a Hash Table-based authentication system for efficient credential lookup.
- Applied file handling to persist account, credential, and transaction data across application sessions.
- Implemented role-based modules for Admin, Staff, and Customer operations.
- Separated data structures, business logic, modules, and utility functions into dedicated directories.
- Used transaction-specific files to maintain individual account transaction records.
- Applied Object-Oriented Programming concepts such as classes, encapsulation, and modular design.

---

## Project Flow

```text
                         ┌──────────────────┐
                         │     BankCore     │
                         │    Application   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    Main Menu     │
                         └────────┬─────────┘
                                  │
                ┌─────────────────┼─────────────────┐
                │                 │                 │
                ▼                 ▼                 ▼
          ┌───────────┐     ┌───────────┐     ┌───────────┐
          │   Admin   │     │   Staff   │     │ Customer  │
          │   Login   │     │   Login   │     │   Login   │
          └─────┬─────┘     └─────┬─────┘     └─────┬─────┘
                │                 │                 │
                └─────────────────┼─────────────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │  Authentication  │
                         │    AuthTable     │
                         │   (Hash Table)   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │  Role-Based      │
                         │     Module       │
                         └────────┬─────────┘
                                  │
              ┌───────────────────┼───────────────────┐
              │                   │                   │
              ▼                   ▼                   ▼
        Admin Operations    Staff Operations    Customer Operations
              │                   │                   │
              └───────────────────┼───────────────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    AccountBST    │
                         │ Binary Search    │
                         │      Tree        │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    FileUtils     │
                         │  File Handling   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Persistent Data  │
                         │     Storage      │
                         └──────────────────┘
```

---

## Project Structure

```text
BankCore/
│
├── data/
│   ├── accounts.txt
│   ├── credentials.txt
│   └── transactions/
│       ├── 1001.txt
│       ├── 1002.txt
│       ├── 1003.txt
│       ├── 1004.txt
│       └── 1005.txt
│
├── include/
│   ├── bst/
│   │   ├── AccountBST.h
│   │   └── AccountNode.h
│   │
│   ├── hashtable/
│   │   ├── AuthTable.h
│   │   ├── BucketNode.h
│   │   └── CredentialNode.h
│   │
│   ├── modules/
│   │   ├── AdminModule.h
│   │   ├── CustomerModule.h
│   │   └── StaffModule.h
│   │
│   └── utils/
│       └── FileUtils.h
│
├── src/
│   ├── bst/
│   │   ├── AccountBST.cpp
│   │   └── AccountNode.cpp
│   │
│   ├── hashtable/
│   │   ├── AuthTable.cpp
│   │   ├── BucketNode.cpp
│   │   └── CredentialNode.cpp
│   │
│   ├── modules/
│   │   ├── AdminModule.cpp
│   │   ├── CustomerModule.cpp
│   │   └── StaffModule.cpp
│   │
│   ├── utils/
│   │   └── FileUtils.cpp
│   │
│   └── main.cpp
│
├── Makefile
├── README.md
└── .gitignore
```

---

## Build and Run

### Prerequisites

Make sure you have:

- C++ Compiler
- Git
- Make

The project uses **C++17** features.

---

## Clone the Repository

Clone the BankCore repository from GitHub:

```bash
git clone https://github.com/divyanshupadhyay83/BankCore.git
```

Navigate to the project directory:

```bash
cd BankCore
```

---

## Compile

Using the provided Makefile:

```bash
make
```

You can also compile the project manually:

```bash
g++ -std=c++17 src/main.cpp src/bst/*.cpp src/hashtable/*.cpp src/modules/*.cpp src/utils/*.cpp -Iinclude -o fintrack
```

---

## Run

On Windows:

```powershell
.\fintrack.exe
```

On Linux / Git Bash:

```bash
./fintrack
```

---

## Data Storage

BankCore uses file handling for persistent storage.

### Accounts

Account information is stored in:

```text
data/accounts.txt
```

### Credentials

Authentication credentials are stored in:

```text
data/credentials.txt
```

### Transactions

Individual account transaction records are stored inside:

```text
data/transactions/
```

For example:

```text
data/transactions/1001.txt
data/transactions/1002.txt
```

This allows transaction information to remain available between application sessions.

---

## Learning Outcomes

Through this project, I gained hands-on experience with:

- Designing applications using Object-Oriented Programming principles
- Implementing Binary Search Trees and Hash Tables
- Working with nodes and linked data structures
- Managing persistent storage using file handling
- Implementing role-based authentication
- Structuring a medium-sized C++ project using modular design
- Applying Data Structures and Algorithms to a real-world application
- Using Git and GitHub for version control

---

## Future Enhancements

- Implement AVL Trees for self-balancing account storage
- Integrate a relational database such as MySQL or PostgreSQL
- Add transaction timestamps and detailed audit logs
- Implement stronger password encryption
- Add OTP-based authentication
- Develop a graphical user interface (GUI)
- Add advanced account search and reporting features
- Add automated backup and recovery
- Develop a web-based version of the application
- Add API-based integration for external services

---

## Author

**Divyansh Upadhyay**

B.Tech Computer Science Engineering Student


## Disclaimer

BankCore is an academic and learning project developed to demonstrate C++ programming, data structures, file handling, authentication, and modular software development.

It is not intended for use as a production banking system.