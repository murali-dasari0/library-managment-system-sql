 Library Management System (MySQL)
 ## Introduction
 The Library Management System is a simple database project built using MySQL Workbench. It
 manages books, members, and borrowed records in a library. This project demonstrates database
 design, table creation, relationships, and SQL queries.
 ## Features- Store book details (title, author, available copies).- Manage members with unique emails.- Track borrowed books with borrow/return dates.- Join queries to fetch complete reports.
 ## Database Design
 The project contains three main tables:
 1. Books - book_id, title, author, available_copies
 2. Members - member_id, name, email
 3. BorrowedBooks - borrow_id, member_id, book_id, borrow_date, return_date
 Relationships:- A member can borrow many books.- A book can be borrowed by many members.
 ## How to Run the Project
 1. Import Database:- Open MySQL Workbench- Go to Server → Data Import- Choose 'Import from Self-Contained File'- Select library_db.sql- Click Start Import
 2. Use Database:
 USE library_db;
 3. Run Queries:
 SELECT * FROM Books;
 SELECT m.name, b.title, bb.borrow_date, bb.return_date
 FROM BorrowedBooks bb
 JOIN Members m ON bb.member_id = m.member_id
 JOIN Books b ON bb.book_id = b.book_id;
 ## Sample Output
 Books Table:
 | book_id | title | author | available_copies |
|--------|----------------|---------------|----------------- |
 | 1 | Harry Potter | J.K. Rowling | 5 |
 | 2 | The Alchemist | Paulo Coelho | 3 |
 | 3 | Atomic Habits | James Clear | 2 |
 ## Tools Used- MySQL Workbench (Database design & queries)- SQL (DDL & DML commands)
 ## Project Highlights- Demonstrates SQL fundamentals: CREATE, INSERT, SELECT, JOIN.- Shows database relationships (primary key, foreign key).- Easy to export/import and run in any system.
