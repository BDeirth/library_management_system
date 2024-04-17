# library_management_system
library_management_system using phpmyadmin/SQL Queries (for database design and data retrieval) and Power BI Desktop (for reports)
This is a small database for a library_management_system using phpmyadmin/SQL queries and Power BI Desktop for a simple report of some of the data collected.

Explanation of the Project:

I created a library management system database. This system contains the information about borrowers, books, copies of books, library branches, loan records, overdue books, and returned books. I created four triggers to automatically update certain aspects of my database.

Returned books trigger:

This trigger automatically updates the returned books table when a return date is added into an entry on the loans table.

Overdue books trigger:

For overdue books I created two triggers; one for after update on the loans table and one for after insert on the loans table. These two check to see if the current date is passed the due date on update and insert within the loans table and if it is then they update
the overdue books table with an entry containing the copy ID, branch ID, and due date of the loan that is overdue.

After book insert trigger:

I created the after_book_insert trigger to add information from the books table into the book copies table after an insert of data on the books table.

There are four library branches:

North, South, East, and West

Each library branch contains a portion of the overall books within the entire system. 

There are a number of borrowers entered with their ID number, first and last name, email, and phone number.

There are multiple copies of the same books so the book copies table is used to keep track of copy ID's for each book ID.

FILES:

library_database_visuals.pdf for viewing of visuals created within Power BI (without access to Power BI)

library_database_visuals.pbix for viewing of visuals created within Power BI (with access to Power BI)

LIBRARY DATABASE MODEL PNG file for a Screenshot of my database model

DATABASE CREATION text document for the initial creation of the database

DATA RETRIEVAL PROCESS text document for the SQL queries I used to retrieve data from the database

DATA INSERTION text document for the SQL queries I used to insert data into the database

DATA RETRIEVED file folder contains the .xls files that I exported once I retrieved the data (each table was exported individually and each 'DR NUM 1' and further file corresponds with the number for each retrieval I outlined in the DATA RETRIEVAL PROCESS text document


