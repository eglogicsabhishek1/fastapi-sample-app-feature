# fastapi-sample-app-feature

📦 Project Description
This project is a FastAPI-based user management system with secure registration, login, and role-based access control.
It uses SQLAlchemy for ORM, MySQL as the database, and Pydantic for data validation.
Features include:

User registration with strong password and email validation
Role assignment (admin/user) with best practices
Secure password hashing (bcrypt + secret key)
JWT-based authentication (if implemented)
Modular code structure for scalability


🚀 Running the Project (Mac, Linux, Windows)
1. Clone the Repository
git clone <your-repo-url>
cd fastapi-sample-app-feature


eglogicsabhishek1
create this project description and runninmg mechanism for mac,linux and windows

GitHub Copilot
Here’s a project description and a universal running guide for Mac, Linux, and Windows:

📦 Project Description
This project is a FastAPI-based user management system with secure registration, login, and role-based access control.
It uses SQLAlchemy for ORM, MySQL as the database, and Pydantic for data validation.
Features include:

User registration with strong password and email validation
Role assignment (admin/user) with best practices
Secure password hashing (bcrypt + secret key)
JWT-based authentication (if implemented)
Modular code structure for scalability
🚀 Running the Project (Mac, Linux, Windows)
1. Clone the Repository
2. Set Up a Virtual Environment
Windows:
python -m venv env
env\Scripts\activate
Mac/Linux:
python3 -m venv env
source env/bin/activate
3.Change directory to module 'app'
 & Install Dependencies
pip install -r requirements.txt
4. Prepare the Database
Make sure MySQL is running and the database exists.
Ensure you have a mysql server installed and initialise the database by executing those 3 SQL scripts. Default configuration: user: test, database name: test, password: test

mysql -u root < database/base/01_init_db.sql
mysql -u root < database/base/02_schema.sql
mysql -u root < database/base/03_data.sql

Run the following SQL to add new columns if needed:
ALTER TABLE users
ADD COLUMN first_name VARCHAR(255) NOT NULL AFTER updated_at,
ADD COLUMN last_name VARCHAR(255) NOT NULL AFTER first_name,
ADD COLUMN email VARCHAR(255) NOT NULL AFTER last_name,
ADD COLUMN phone VARCHAR(50) NOT NULL AFTER email;

6. Run the Application
Windows:
uvicorn app.main:app --reload --host 0.0.0.0 --port 8080

Mac/Linux:
uvicorn app.main:app --reload --host 0.0.0.0 --port 8080


