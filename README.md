# 🚀 FastAPI Sample App - User Management System

A **FastAPI-based user management system** with secure registration, login, and role-based access control. Built for scalability and clean architecture using:

- ✅ **FastAPI** – modern Python web framework  
- ✅ **SQLAlchemy** – powerful ORM for database operations  
- ✅ **MySQL** – relational database  
- ✅ **Pydantic** – for data validation  
- ✅ **bcrypt** – for secure password hashing  
- ✅ **JWT** (optional) – for token-based authentication  

## 📦 Features

- 🔐 User registration with strong password and email validation  
- 👥 Role assignment (admin/user)  
- 🛡️ Secure password hashing using `bcrypt` + secret key  
- 🔑 JWT-based authentication (optional)  
- 📁 Modular and scalable code structure  

## 💻 Getting Started (Mac, Linux, Windows)

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd fastapi-sample-app-feature
2. Create & Activate Virtual Environment
Windows
python -m venv env
env\Scripts\activate
Mac/Linux
python3 -m venv env
source env/bin/activate
3. Install Dependencies
pip install -r requirements.txt
4. Prepare the MySQL Database
Ensure MySQL is running. Default credentials:

User: test

Password: test

Database: test

Run the following SQL scripts:
mysql -u root -p < database/base/01_init_db.sql
mysql -u root -p < database/base/02_schema.sql
mysql -u root -p < database/base/03_data.sql

Add extra columns to users table:
ALTER TABLE users
ADD COLUMN first_name VARCHAR(255) NOT NULL AFTER updated_at,
ADD COLUMN last_name VARCHAR(255) NOT NULL AFTER first_name,
ADD COLUMN email VARCHAR(255) NOT NULL AFTER last_name,
ADD COLUMN phone VARCHAR(50) NOT NULL AFTER email;


5. Run the Application
uvicorn main:app --reload --port 8081


