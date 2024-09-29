# Student Management System

This project is a Student Management System built using Python and MySQL (for the database). It allows educational institutions to manage student records efficiently with options to add, update, delete, search, and view records. The project aims to solve internal school issues like managing admissions, student information, and teacher records.

# Features

	•	View Records: Displays all non-deleted student records from the database, showing ID, name, roll number, and contact details.
	•	Insert Record: Adds a new student record after verifying that the roll number is unique and validating the input fields.	
	•	Delete Record: Soft deletes a record by marking it as deleted in the database without permanently removing it.
	•	Search Record: Allows users to search for a student by ID, name, roll number, or contact details.
	•	Update Record: Fetches a specific student record and allows the user to update any of the student’s details after verification.
	•	Input Validation: Validates all user inputs for proper format and correct data types (e.g., numeric contact, roll number format like SE-2020-053).

# Technologies Used

	•	Backend: Python
	•	Database: MySQL

Database Schema

	•	Table: Students
	•	Id: Primary key, auto-incremented.
	•	Name: Student’s name (max 20 characters).
	•	RollNo: Student’s roll number (format: SE-YYYY-XXX).
	•	Contact: 11-digit numeric contact number.
	•	IsDeleted: Boolean field (0 = active, 1 = deleted).

How to Use

	1.	Clone the repository.
	2.	Install the necessary dependencies using pip install mysql-connector-python.
	3.	Set up the MySQL database and create a Students table (schema provided above).
	4.	Update database credentials in the main script (mydb connection).
	5.	Run the Python script to launch the system.
	6.	Choose from the menu options to interact with the system.

Example Queries:

	•	View records: SELECT * FROM Students WHERE IsDeleted = 0;
	•	Insert new record: INSERT INTO Students (Name, RollNo, Contact) VALUES (%s, %s, %s);
	•	Search by RollNo: SELECT * FROM Students WHERE RollNo = %s AND IsDeleted = 0;
	•	Soft delete a record: UPDATE Students SET IsDeleted = 1 WHERE Id = %s;

This project is an example of how to integrate a MySQL database with Python to manage records in a simple and efficient way.
