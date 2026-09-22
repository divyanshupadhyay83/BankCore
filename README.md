# BankCore

BankCore is a console-based banking management application developed in C++. 
The project provides a structured system for managing customer accounts, 
authentication, banking operations, and account-related information.

The project demonstrates the use of important C++ concepts and Data Structures 
such as Object-Oriented Programming, Binary Search Tree (BST), Hash Tables, 
File Handling, Modular Programming, and Makefile-based compilation.

---

## Features

### Customer Module
Customers can perform banking-related operations through their account.

- Customer login and authentication
- View account details
- Check account balance
- Deposit money
- Withdraw money
- Transfer money to another account
- View transaction history
- Manage account-related operations

### Staff Module

Staff members can manage customer accounts and perform staff-level operations.

- Staff authentication
- View customer account information
- Manage customer-related operations
- Access account records
- Perform authorized banking operations

### Admin Module

The administrator has access to administrative operations.

- Admin authentication
- Manage bank accounts
- View account records
- Manage staff/customer-related information
- Perform administrative operations

---

## Technologies Used

- **Programming Language:** C++
- **Data Structures:**
  - Binary Search Tree (BST)
  - Hash Table
  - Linked List / Node-based structures
- **Concepts:**
  - Object-Oriented Programming
  - File Handling
  - Authentication
  - Modular Programming
  - Exception/Error Handling
- **Storage:** Text files
- **Build System:** Makefile

---

## Project Architecture

The project is organized into separate directories for better maintainability.

```text
BankCore/
│
├── data/
│   ├── accounts.txt
│   ├── credentials.txt
│   │
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
├── .gitignore
├── Makefile
└── README.md
