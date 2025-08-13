# Library-Mangement-system-using--sql

# 📚 Library Management System (SQL Project)

## 📌 Overview
The **Library Management System** is a basic-to-intermediate SQL project that manages books, library members, and book borrowing activities.  
It demonstrates how to design a relational database, populate it with data, and run queries to retrieve useful information.

---

## 🎯 Features
- Store and manage book details (title, author, genre, copies available, etc.)
- Maintain member records (name, email, join date)
- Track borrowed books with borrow and return dates
- Perform queries for:
  - Available books
  - Borrowed books with member names
  - Number of books borrowed per member
  - Updating available copies after borrowing
  - Deleting returned borrow records

---

## 🗄 Database Structure
### **Tables**
1. **Books**
   - `book_id` (Primary Key)
   - `title`
   - `author`
   - `genre`
   - `published_year`
   - `available_copies`

2. **Members**
   - `member_id` (Primary Key)
   - `name`
   - `email`
   - `join_date`

3. **BorrowedBooks**
   - `borrow_id` (Primary Key)
   - `member_id` (Foreign Key → Members)
   - `book_id` (Foreign Key → Books)
   - `borrow_date`
   - `return_date`

---

## 💾 Sample Queries

### 1️⃣ Get all available books
```sql
SELECT title, author, available_copies
FROM Books
WHERE available_copies > 0;
