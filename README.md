# 🏦 Bank Account Management System

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Swing](https://img.shields.io/badge/Java_Swing-GUI-blue?style=for-the-badge)

> A complete desktop-based Bank Account Management System built during **Hindalco Summer Training 2025** at **Aditya Birla Group**.

-----

## 👨‍💻 Project Details

|                |                                                              |
|----------------|--------------------------------------------------------------|
|**Developer**   |Durgesh Kumar Singh                                           |
|**Degree**      |B.Tech — Artificial Intelligence & Data Science (7th Semester)|
|**Supervisor**  |Mr. Mukul Srivastava                                          |
|**Organization**|Hindalco Industries Ltd (Aditya Birla Group)                  |
|**Year**        |2025                                                          |

-----

## 📌 About The Project

The **Bank Account Management System** is a fully functional desktop banking application that simulates real-world banking operations. Built using **Java Swing** for the GUI and **MySQL** for the database, this project covers all core banking functionalities that a customer would need.

The system is designed with two modules:

- **Admin Module** — Full control over all accounts and transactions
- **User Module** — Customer-facing ATM-style interface

-----

## ✨ Key Features

### 🔐 Authentication

- Secure login with Card Number and PIN
- New account registration (3-step application form)
- PIN change functionality

### 💰 Banking Operations

- Deposit money
- Cash withdrawal (with balance validation)
- Fast Cash (preset withdrawal amounts — ₹100 to ₹10,000)
- Balance enquiry
- Mini statement (transaction history)

### 👤 Account Management

- 3-page account application form
- Personal details (Name, DOB, Gender, Address)
- Additional details (Religion, Category, PAN, Aadhar)
- Account type selection (Savings, Current, Fixed Deposit, Recurring)
- Services selection (ATM Card, Internet Banking, Mobile Banking, etc.)

### 📊 Admin Features

- View all accounts
- Manage transactions
- Activate/deactivate accounts
- View complete transaction histories

-----

## 🛠️ Tech Stack

|Technology      |Purpose                                          |
|----------------|-------------------------------------------------|
|**Java**        |Core programming language                        |
|**Java Swing**  |GUI framework for desktop interface              |
|**MySQL**       |Database for storing account and transaction data|
|**JDBC**        |Java Database Connectivity                       |
|**JDateChooser**|Date picker component                            |

-----

## 🗄️ Database Schema

### Tables Used:

- `login` — Stores card number and PIN
- `signup` — Personal details (Page 1)
- `signup2` — Additional details (Page 2)
- `signup3` — Account details (Page 3)
- `bank` — Transaction records

-----

## 🚀 How To Run This Project

### Prerequisites

- Java JDK 8 or higher installed
- MySQL Server installed
- MySQL Connector JAR added to project

### Step 1 — Clone the repository

```bash
git clone https://github.com/yourusername/Bank-Management-System.git
```

### Step 2 — Setup MySQL Database

```sql
CREATE DATABASE bankmanagement;
USE bankmanagement;

CREATE TABLE login (
    formno VARCHAR(20),
    cardno VARCHAR(20),
    pin VARCHAR(10)
);

CREATE TABLE signup (
    formno VARCHAR(20),
    name VARCHAR(50),
    fname VARCHAR(50),
    dob VARCHAR(20),
    gender VARCHAR(10),
    email VARCHAR(50),
    marital VARCHAR(20),
    address VARCHAR(100),
    city VARCHAR(30),
    pincode VARCHAR(10),
    state VARCHAR(30)
);

CREATE TABLE signup2 (
    formno VARCHAR(20),
    religion VARCHAR(20),
    category VARCHAR(20),
    income VARCHAR(30),
    education VARCHAR(30),
    occupation VARCHAR(30),
    pan VARCHAR(20),
    aadhar VARCHAR(20),
    scitizen VARCHAR(5),
    eaccount VARCHAR(5)
);

CREATE TABLE signup3 (
    formno VARCHAR(20),
    atype VARCHAR(30),
    cardno VARCHAR(20),
    pin VARCHAR(10),
    facility VARCHAR(100)
);

CREATE TABLE bank (
    pin VARCHAR(10),
    date VARCHAR(50),
    mode VARCHAR(20),
    amount VARCHAR(20)
);
```

### Step 3 — Configure Database Connection

Open `Conn.java` and update:

```java
Connection c = DriverManager.getConnection(
    "jdbc:mysql://localhost/bankmanagement", 
    "root",      // your MySQL username
    "Du31@singh"   // your MySQL password
);
```

### Step 4 — Run The Project

```bash
javac Login.java
java Login
```

Or run directly from your IDE (Eclipse/IntelliJ).

-----

## 📸 Screenshots

### ATM Login Screen

![Login](screenshots/login.png)

### Account Application Form

![Signup](screenshots/signup.png)

### Transaction Menu

![Transactions](screenshots/transactions.png)

### Deposit Screen

![Deposit](screenshots/deposit.png)

### Fast Cash Screen

![FastCash](screenshots/fastcash.png)

### Withdrawal Screen

![Withdrawal](screenshots/withdrawal.png)

### PIN Change Screen

![PINChange](screenshots/pinchange.png)

-----

## 📂 Project Structure

```
Bank-Management-System/
├── src/
│   └── bank/management/system/
│       ├── Login.java          → ATM login screen
│       ├── Signup.java         → Registration page 1
│       ├── Signup2.java        → Registration page 2
│       ├── Signup3.java        → Registration page 3
│       ├── Transactions.java   → Main transaction menu
│       ├── Deposit.java        → Deposit functionality
│       ├── Withdrawl.java      → Withdrawal functionality
│       ├── FastCash.java       → Quick cash withdrawal
│       ├── Pin.java            → PIN change
│       ├── BalanceEnquiry.java → Check balance
│       ├── MiniStatement.java  → Transaction history
│       └── Conn.java           → Database connection
├── icons/
│   ├── logo.png
│   └── atm.jpg
├── screenshots/
└── README.md
```

-----

## 🔑 How To Use

1. **New User** — Click “Sign Up” → Fill 3-page form → Get Card Number & PIN
1. **Existing User** — Enter Card Number + PIN → Select transaction
1. **Deposit** — Select Deposit → Enter amount → Confirm
1. **Withdraw** — Select Cash Withdrawal → Enter amount → Confirm
1. **Fast Cash** — Select Fast Cash → Choose preset amount
1. **Check Balance** — Select Balance Enquiry
1. **View History** — Select Mini Statement
1. **Change PIN** — Select PIN Change → Enter new PIN twice

-----

## 💡 What I Learned

Building this project at Hindalco gave me hands-on experience with:

- **Java OOP concepts** — Classes, inheritance, interfaces
- **GUI development** — Java Swing components and event handling
- **Database integration** — JDBC, SQL queries, ResultSet handling
- **Real-world banking logic** — Transaction validation, balance checks
- **Software development lifecycle** — Requirements, design, implementation, testing
- **Corporate environment** — Working under professional supervision at Aditya Birla Group

-----

## 🏢 About Hindalco

Hindalco Industries Limited is a subsidiary of the Aditya Birla Group and is one of the world’s largest aluminium rolling companies and a major copper producer. This project was developed as part of the Summer Training Programme 2025.

-----

## 📞 Contact

**Durgesh Kumar Singh**

- 🎓 B.Tech — AI & Data Science, 7th Semester
- 📧 [your email here]
- 💼 [your LinkedIn here]
- 🐙 [your GitHub here]

-----

## 📄 License

This project was developed for educational purposes during summer training at Hindalco Industries Ltd.

-----

*Built with ❤️ during Hindalco Summer Training 2025*
