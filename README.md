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
- Applied Object-Oriented Programming concepts such as classes, encapsulation, abstraction, inheritance, and polymorphism where applicable.

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
                         │ Role-Based       │
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
cd BankCore
make
g++ -std=c++17 src/main.cpp src/bst/*.cpp src/hashtable/*.cpp src/modules/*.cpp src/utils/*.cpp -Iinclude -o fintrack

Author

Divyansh Upadhyay

B.Tech Computer Science Engineering Student
