# 📚 FastAPI Library Book Management System

## 🚀 Project Overview

The **Library Book Management System** is a backend application built using **FastAPI** that allows a library to manage books, borrowing activities, and member interactions efficiently.

This project was developed as part of the **FastAPI Internship Program** where multiple backend concepts such as API design, data validation, CRUD operations, workflows, search, sorting, and pagination were implemented.

The system simulates how a real-world library backend works by allowing users to:

* View books
* Borrow books
* Return books
* Join a waiting queue
* Search and filter books
* Browse data using sorting and pagination

All APIs are tested using **Swagger UI**.

---

# 🛠 Technologies Used

| Technology     | Purpose                            |
| -------------- | ---------------------------------- |
| **Python**     | Core programming language          |
| **FastAPI**    | Backend API framework              |
| **Pydantic**   | Data validation and request models |
| **Uvicorn**    | ASGI server for running FastAPI    |
| **Swagger UI** | API testing and documentation      |

---

# 📂 Project Structure

```
fastapi-library-book-system
│
├── main.py
├── requirements.txt
├── README.md
└── screenshots
      ├── Q1_home_route.png
      ├── Q2_get_all_books.png
      ├── Q3_get_book_by_id.png
      ├── ...
      └── Q20_browse_endpoint.png
```

---

# ⚙️ Installation & Setup

Follow these steps to run the project locally.

### 1️⃣ Clone the Repository

```
git clone https://github.com/Varshithchidurala/fastapi-library-book-system.git
```

### 2️⃣ Navigate to Project Folder

```
cd fastapi-library-book-system
```

### 3️⃣ Create Virtual Environment

```
python -m venv venv
```

### 4️⃣ Activate Virtual Environment

Windows:

```
venv\Scripts\activate
```

Mac/Linux:

```
source venv/bin/activate
```

### 5️⃣ Install Dependencies

```
pip install -r requirements.txt
```

### 6️⃣ Run FastAPI Server

```
uvicorn main:app --reload
```

### 7️⃣ Open Swagger API Docs

```
http://127.0.0.1:8000/docs
```

---

# 📌 API Features Implemented

## 🔹 Basic APIs

* Home route
* Get all books
* Get book by ID
* Books summary statistics

## 🔹 Borrow Management

* Borrow books
* View borrow records
* Borrow queue system
* Return books and auto-assign to waiting members

## 🔹 CRUD Operations

* Add new book
* Update book availability and genre
* Delete book
* Duplicate title validation

## 🔹 Helper Functions

Custom helper functions were used to keep the code clean:

* `find_book()`
* `calculate_due_date()`
* `filter_books_logic()`

---

# 🔍 Advanced API Features

## Search

Search books by keyword across:

* Title
* Author

Example:

```
/books/search?keyword=python
```

---

## Sorting

Books can be sorted by:

* title
* author
* genre

Example:

```
/books/sort?sort_by=title&order=asc
```

---

## Pagination

Books can be browsed page by page.

Example:

```
/books/page?page=1&limit=3
```

---

## Combined Browse Endpoint

A powerful endpoint that combines:

* Search
* Sorting
* Pagination

Example:

```
/books/browse?keyword=python&sort_by=title&page=1&limit=2
```

---

# 🔄 Multi-Step Workflow

This project implements a **real library workflow**:

```
Borrow Book
      ↓
Book becomes unavailable
      ↓
Users join queue
      ↓
Book returned
      ↓
First queued user automatically borrows
```

---

# 📸 API Testing

All APIs were tested using **Swagger UI**.

Example endpoints tested:

* `/books`
* `/books/{book_id}`
* `/books/filter`
* `/books/search`
* `/books/page`
* `/books/browse`
* `/borrow`
* `/return/{book_id}`
* `/queue/add`

Screenshots of each endpoint are available in the **screenshots folder**.

---

# 🎯 Internship Learning Outcomes

Through this project, I gained hands-on experience in:

* Designing REST APIs
* Implementing backend workflows
* Data validation using Pydantic
* Structuring FastAPI applications
* Implementing search, sorting, and pagination
* Testing APIs using Swagger documentation

---

# 👨‍💻 Author

**Varshith Ch**

FastAPI Internship Project

---

# 🙏 Acknowledgment

This project was developed as part of training provided by:

**Innomatics Research Labs**

