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

