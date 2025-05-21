# Library-Management-System
A Library Management System built entirely using MySQL Workbench, focusing on database design and SQL queries. It includes tables for books, members, issues, and returns, with efficient data handling using SQL operations.

# 📚 Library Management System (MySQL Project)

This is a **Library Management System** project built entirely using **MySQL Workbench**. It focuses on database schema design, normalization, and SQL query implementation to efficiently manage library operations such as tracking books, members, issue and return records.

![MySQL](https://img.shields.io/badge/Database-MySQL-blue?logo=mysql)
![Status](https://img.shields.io/badge/Project%20Status-Completed-brightgreen)
![IDE](https://img.shields.io/badge/IDE-MySQL%20Workbench-orange?logo=mysql)

---

## 🧩 Features

- Structured and normalized database design  
- Tables for books, members, issue records, and returns  
- Primary and foreign key constraints for data integrity  
- SQL queries for:
  - Adding/removing books and members  
  - Issuing and returning books  
  - Viewing currently issued books  
  - Generating reports (e.g., overdue books, member borrowing history)

---

## 🗂️ Database Tables

| Table Name      | Description                                 |
|------------------|---------------------------------------------|
| `books`          | Stores details of all books in the library |
| `members`        | Stores library user/member data             |
| `issue_records`  | Tracks which book is issued to whom and when|
| `return_records` | Tracks return date and late fine (if any)   |

---

## ⚙️ Tools Used

- **MySQL Workbench**  
- **SQL** (DDL, DML, and DQL queries)

---

## 🛠️ How to Use

1. **Open MySQL Workbench**
2. **Create a new schema** (e.g., `library_db`)
3. **Run the SQL script** provided in the repository to:
   - Create tables
   - Insert sample data
   - Execute queries to test functionality

---

## 🚀 Sample SQL Queries

```sql
-- Issue a book
INSERT INTO issue_records (member_id, book_id, issue_date)
VALUES (1, 101, CURDATE());

-- Return a book
INSERT INTO return_records (issue_id, return_date)
VALUES (10, CURDATE());

-- View all issued books
SELECT b.title, m.name, i.issue_date
FROM issue_records i
JOIN books b ON i.book_id = b.book_id
JOIN members m ON i.member_id = m.member_id;
👨‍💻 Developed By
Rakesh Kudachi
Database Developer
Email: rakeshkudachi2526@gmail.com
Location: Ainapur, Belagavi, Karnataka, India

📄 License
This project is created for academic and learning purposes.
Feel free to use and modify for your own database practice.

