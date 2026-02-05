# Student Management System (PyQt6 + MySQL)

A desktop-based **Student Management System** built using **Python**, **PyQt6**, and **MySQL**.  
This application allows users to **add, view, update, delete, and search student records** using a graphical interface.

---

## Features

- Add new students
- View all student records
- Update existing student details
- Delete student records
- Search students by name
- MySQL database integration
- PyQt6-based GUI

---

## Tech Stack

- **Python 3.9+**
- **PyQt6**
- **MySQL 8.x**
- **mysql-connector-python**

---

## Project Structure

```text
StudentDatabaseWithMySQL/
│
├── main.py                 # Main PyQt6 application
├── database_login.py       # MySQL connection credentials
├── README.md               # Project documentation
│
├── icons/                  # Toolbar icons
│   ├── add.png
│   └── search.png
```

---

## Prerequisites

### Ensure the following are installed:

- Python 3.9 or higher
- MySQL Server
- pip (Python package manager)

### Verify installations:

```bash
python --version
mysql --version
```

---

## Python Dependencies

### Install required packages:

```text
pip install PyQt6 mysql-connector-python
```

---

## Database Setup (MySQL)

### Login to MySQL

```text
#Login to MySQL
mysql -u root -p

#Create database
CREATE DATABASE school;

#Use database
USE school;

#Create students table
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    course VARCHAR(50) NOT NULL,
    mobile VARCHAR(15) NOT NULL
);

#Verify tables
SHOW TABLES;                           
DESCRIBE students;
```

---

## Database Configuration

Create a file named database_login.py in the project root directory.

```text
database_login.py
host = "localhost"
user = "root"
password = "YOUR_MYSQL_PASSWORD"
database = "school"
```

---

## Running the Application

### Activate the virtual environment:

```text
source .venv/bin/activate
```

### Run the application:

```text
python main.py
```
