# Assignment

# Files, Exceptions, and SQL

In this assignment, you'll read from data files, process the data, and write to output files. We'll also look at using Python to work with light-weight, file-based relational database SQLite using the sqlite3 module from the Python Standard Library.

# Chapters

Work through the book and examples from Chapters 9 and 17.2 (SQL).

# Data At Rest

This module deals with _data at rest_. Data at rest may be kept in:

- files,
- relational databases (e.g., SQLite, SQL Server, Oracle),
- NoSQL datastores (e.g., MongoDB)
- Graph databases (e.g., Neo4J)
- and more.

We'll look at how to read and write from files and relational databases.

Data at rest is only part of the story. In analytics, there is also _data in motion_. _Data in motion_ is unbounded - infinite - and is covered in our program course on Streaming Data.

# Get Started

1. Log in to your GitHub account.
2. Create a new GitHub repo named  **datafun-05-data-at-rest**. Follow conventions - use kebob, lower case, no spaces.
3. Git clone your new repo into your Documents folder.
4. Always ensure your repo has the 3 basic files all our repos need:
  1. a good README.md,
  2. .gitignore, and
  3. about.py.
5. Copy these from previous repos as needed.
6. Update README.md to reflect the focus of this module.

Authors examples: You're encouraged to use the authors examples for practice. Use these right from your local IntroToPython directory - don't commit the author's work into your repo.

# Task 1

**Read and work through Chapter 9 - Files & Exceptions - understand the examples. **

- 9.1 Introduction
- 9.2 Files
- 9.3 Text-File Processing
  - 9.3.1 Writing to a Text File: Introducing the with Statement
  - 9.3.2 Reading Data from a Text File
- 9.4 Updating Text Files
- 9.5 Serialization with JSON
- 9.6 Focus on Security: pickle Serialization and Deserialization
- 9.7 Additional Notes Regarding Files
- 9.8 Handling Exceptions
  - 9.8.1 Division by Zero and Invalid Input
  - 9.8.2 try Statements
  - 9.8.3 Catching Multiple Exceptions in One except Clause
  - 9.8.4 What Exceptions Does a Function or Method Raise?
  - 9.8.5 What Code Should Be Placed in a try Suite?
- 9.9 finally Clause
- 9.10 Explicitly Raising an Exception
- 9.11 (Optional) Stack Unwinding and Tracebacks
- 9.12 Intro to Data Science: Working with CSV Files
  - 9.12.1 Python Standard Library Module csv
  - 9.12.2 Reading CSV Files into Pandas DataFrames
  - 9.12.3 Reading the Titanic Disaster Dataset
  - 9.12.4 Simple Data Analysis with the Titanic Disaster Dataset
  - 9.12.5 Passenger Age Histogram

# Task 2

**Read and work through Chapter 17 - Big Data - understand the examples. **

- 17.1 Introduction
- 17.2 Relational Databases and Structured Query Language (SQL)
  - 17.2.1 A books Database
  - 17.2.2 SELECT Queries
  - 17.2.3 WHERE Clause
  - 17.2.4 ORDER BY Clause
  - 17.2.5 Merging Data from Multiple Tables: INNER JOIN
  - 17.2.6 INSERT INTO Statement
  - 17.2.7 UPDATE Statement
  - 17.2.8 DELETE FROM Statement

# Task 3 - Titanic (from 9.12 above)

1. Follow the instructions in 9.12.3 (starting pg. 346).
2. Don't work in interactive mode!
3. Instead complete the exercise in a  **notebook**.
4. 1-Load: Use pandas to read in the Titanic Disaster dataset csv file.
5. 2-View: Set the precision to 2 decimal places. View the head and tail of the file.
6. 3-Headings: customize the column headings.
7. 4-Describe: Use the DataFrame describe() function to calculate basic descriptive statistics for all numeric columns.
8. 5-Survivors: Follow instructions to describe statistics for those who survived (titanic.survived == 'yes') - see the example.
9. Notice that describe provides different results for non-numeric data (e.g., unique, top, freq)
10. Enable matplotlib. If it doesn't work (e.g., in a notebook), try

%matplotlib inline

1. 6-Histogram: Use the DataFrame's hist() function to create a histogram for each numerical column.
2. Required: Use Section headings in your Markdown to make it clear that each of these 6 sections are shown in your notebook. They should be numbered 1-6 and include the keyword shown above.
3. Required: Include the title of the notebook, and your name and date at the top.
4. Do these consistently. A heading and section titles is required in every notebook.

# Task 3 Output

Document your results.

- execute the completed notebook
- export to html
- include the html in your repo

# Task 4 - SQL (from 17.2 above)

1. Follow the instructions in 17.2.1 (starting pg 730)
2. Don't work in interactive mode - use a notebook.
3. IMPORTANT: create the table using the books.sql script provided with the author files.  See [https://github.com/pdeitel/IntroToPython/blob/master/examples/ch17/sql/books.sqlLinks to an external site.](https://github.com/pdeitel/IntroToPython/blob/master/examples/ch17/sql/books.sql)
4. Import the sqlite3 module and use the connect function to create a connection to your database.
5. After running the script, there should be 3 tables: authors, author\_ISBN, and titles.
6. Import pandas as pd
7. Use pd options.display to set the max\_columns to 10
8. Use pd read\_sql fuction to select everything (\*) from the authors table, then the titles table, then the author\_ISBN table.
9. Complete 17.2.2 SELECT (1 query)
10. Complete 17.2.3 WHERE (3 queries)
11. Complete 17.2.4 ORDER BY (4 queries)
12. Complete 17.2.5 INNER JOIN (1 query)
13. Complete 17.2.6 INSERT INTO (2 queries)
14. Complete 17.2.7 UPDATE (2 queries)
15. Complete 17.2.8 DELETE FROM (2 queries)
16. Final Results, SELECT \* from each table and display the final state of each of the 3 tables.
17. Required: Use Section headings in your Markdown to make it clear that each of these 8 sections are shown in your notebook. They should be numbered 1-8 and include the SQL keyword shown above. Use a heading before your the final results showing all 3 tables as well.
18. Required: Include the title of the notebook, and your name and date at the top.
19. Do these consistently. A heading and section titles is required in every notebook.

# Task 4 Output

Document your results.

- execute the completed notebook
- export to html
- include the html in your repo

# Task 5. Push Repo to GitHub

Use VS Code to commit and sync (push) your repo to GitHub - or in Git Bash or terminal, do the following.

git add .
 git commit -m "added code"
 git push origin main

# Optional Task 6. Bonus

1. Start a new notebook.
2. Locate a unique csv dataset.
3. Use pandas to import the csv dataset into a DataFrame.
4. Use the DataFrame commands to clean the data as needed and/or rename the columns.
5. Use the DataFrame describe() function to calculate basic descriptive statistics.
6. Use the DataFrame hist() function to generate histograms for all numeric columns.
7. Include the required heading at the top, and use section headings to tell your story with data.
8. Execute the entire, professionally presented file and output to html.
9. Git add, git commit, and git push the new content to your GitHub repo.

# Checklist
Change the open boxes [ ] below to checked boxes [x] as you complete the tasks.

- [x] Task 1. Read and work through Chapter 9 - Files & Exceptions - understand the examples.
- [x] Task 2. Read and work through Chapter 17 - Big Data - understand the examples.
- [x] Task 3 - Titanic (from 9.12 above)
- [x] Task 3 - #Task 3 Output
- [x] Task 4. SQL (from 17.2 above)
- [x] Task 4. Task 4 Output
- [x] Task 5. Push Repo to GitHub
- [x] Task 6. Optional Bonus


Finally - after your initial commit and push, you can check the last box. Check the box, commit your changes (with a message!), and push/sync again.