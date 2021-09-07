# Modern-Big-Data-Analysis-with-SQL-Specialization
All three assignments for Modern Big Data Analysis with SQL Specialization.

# Assignment 1: Foundations for Big Data Analysis with SQL

Include your name and the date at the top of your document. (In a real world setting it's important to know whom to ask if there are questions, and to note whether the document reflects changes made after a certain date.)

Provide the name of the database you're overviewing (in this case, the fun database).

List all tables in the database. For each table, provide a phrase with your best determination of the table's content.

Provide a separate section for each table, giving:
The table name 
The table schema, with a) each column name (make sure to include all columns for each table); b) each column data type; and c) brief notes about the column. (Use your judgement about what comments may be useful here, such as PK, FK, meaning of the data, guesses or questions about the unit of measure or monetary unit. You do not need a comment for every column, but do include some column comments in this document.)

A few sample rows from the table Include a statement about whether the comments on your tables and columns are official from the data sources, or are yourown determination about the data. (In this case, you are providing comments based on your initial investigation of the data. In a real world setting you may obtain some comments officially from the data originators.)

# Assignment 2: Analyzing Big Data with SQL

Your job is to recommend which pair of United States airports should be connected with a high-speed passenger rail tunnel. The company you work for has given you the following strict requirements:

These two airports must:

Be between 300 and 400 miles apart
Average at least 5,000 (five thousand) flights per year between them, in each direction
Among the pairs of airports that meet these requirements, you must identify the one pair that has the largest total number of seats on the planes that flew between them.

The company is also interested to know the average arrival delay for flights between these two airports, because they believe that routes with a history of delayed arrivals will make it easier to persuade air travelers to switch to high-speed rail.

For the pair of airports you recommend, you must provide the following details:

The three-letter codes identifying both airports
The average flight distance in miles for flights between the airports, in each direction
The average number of flights per year between the airports, in each direction
The average annual passenger capacity (average yearly total number of seats on the planes) for flights between the airports, in each direction
The average arrival delay for flights between the airports, in each direction

You must write a SELECT statement to identify the pair of airports that fulfills all the requirements listed above. This SELECT statement must also return all the required details listed above.

The following hints might help you:

The flights table has a column named distance which gives the distance in miles of each flight. Use the values in this column as the distances between airports.
The planes table contains ten years of flights data, so to get per-year (annual) average totals, divide the full-table totals by ten.
The planes table has a column named seats which gives the number of seats on each plane.
The first two rows in the result of your query should show your recommended tunnel route. These top two rows should both show the same pair of airports, but with the origin and dest switched.

# Assignment 3: Managing Big Data in Clusters and Cloud Storage

Use the commands you learned about in this course to list and examine the three files containing the tunnel boring machine data. They are delimited text files, each containing tens of thousands of lines. They are stored in Amazon S3 in subdirectories under a directory named tbm_sf_la in the S3 bucket named training-coursera2. You have read access to this bucket.

Hint: List these files and view their contents by running commands in the terminal. Use chaining to apply the head command to display only the first few rows of each file.

Notice what these three files have in common:

Each file contains eight columns representing the same eight fields
The data types of the eight columns are the same in all three files
The rows of the table represent hourly time intervals
Notice the differences between these three files:

They use different delimiters
One of the files uses the string 999999 to represent missing values
One of the files has a header line
Create the Table
Create a table named tbm_sf_la in the database named dig to store the data from all three of the TBMs. Use what you learned by examining the data to decide how best to do this.

W​hen creating this table, you must:

Use the exact column names shown in the header line in one of the files
Specify appropriate data types for the columns, based on what you observed when examining the data and based on what you have learned about data types in this course
Ensure that the table can be queried by both Hive and Impala
Remember that all the files in one table's storage directory should be uniformly formatted; they should all use the same delimiter, they should all use the same strings to represent missing values, and they should either all have a header line or none of them should. However, the files in S3 are not uniformly formatted, so you cannot simply copy the three files to the new table's directory.

Hint: You might decide to create three separate tables (one for each TBM) as an intermediate step before creating one table to store the data for all three TBMs.

Keep in mind that there are many different ways to successfully complete this task. Think about everything you have learned in this course and consider alternative approaches.

Load the Data into the Table
Load the data for all three TBMs into the table. That this might be a one-step process or a multi-step process—or it might not be necessary at all—depending on what approach you decided to use. Keep track of all the commands and statements you run, so that you can include them all in the document.

Run some SELECT queries on the resulting table and check that they return the expected results.




