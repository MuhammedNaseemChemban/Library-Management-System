# Library Management System

## Overview

This project is a Library Management System designed to keep track of all information about books in the library, including their availability, cost, and the total number of books. The system also manages employee details, customer information, and the status of book issues and returns.

## Features

- Manage branches of the library
- Track employees and their details
- Maintain a catalog of books with rental prices and availability
- Manage customer registrations and their issued books
- Monitor the status of book issues and returns

## Database Structure

The project includes the following tables in the `library` database:

1. **Branch**
   - `Branch_no` (Primary Key)
   - `Manager_Id`
   - `Branch_address`
   - `Contact_no`

2. **Employee**
   - `Emp_Id` (Primary Key)
   - `Emp_name`
   - `Position`
   - `Salary`
   - `Branch_no` (Foreign Key)

3. **Books**
   - `ISBN` (Primary Key)
   - `Book_title`
   - `Category`
   - `Rental_Price`
   - `Status` (Available/Not Available)
   - `Author`
   - `Publisher`

4. **Customer**
   - `Customer_Id` (Primary Key)
   - `Customer_name`
   - `Customer_address`
   - `Reg_date`

5. **IssueStatus**
   - `Issue_Id` (Primary Key)
   - `Issued_cust` (Foreign Key)
   - `Issued_book_name`
   - `Issue_date`
   - `ISBN_book` (Foreign Key)

6. **ReturnStatus**
   - `Return_Id` (Primary Key)
   - `Return_cust`
   - `Return_book_name`
   - `Return_date`
   - `ISBN_book2` (Foreign Key)

## SQL Queries

The following SQL queries can be used to interact with the database:

1. Retrieve the book title, category, and rental price of all available books.
2. List the employee names and their respective salaries in descending order.
3. Retrieve the book titles and the corresponding customers who have issued those books.
4. Display the total count of books in each category.
5. Retrieve the employee names and their positions for employees whose salaries are above Rs. 50,000.
6. List the customer names who registered before `2022-01-01` and have not issued any books.
7. Display the branch numbers and the total count of employees in each branch.
8. Display the names of customers who have issued books in the month of June 2023.
9. Retrieve book titles from the book table containing "history."
10. Retrieve branch numbers along with the count of employees for branches having more than 5 employees.
11. Retrieve the names of employees who manage branches and their respective branch addresses.
12. Display the names of customers who have issued books with a rental price higher than Rs. 25.

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/MuhammedNaseemChemban/library-management-system.git
