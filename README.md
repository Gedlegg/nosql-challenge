# nosql-challenge

## Project Overview
This challenge involves setting up a MongoDB database, importing data, updating data, and performing exploratory data analysis using a Jupyter Notebook. The database contains information about food establishments in the UK. The challenge is divided into three main parts:

## Part 1: Database and Jupyter Notebook Setup
-  The `mongoimport` command is used to import the `establishments.json` file into the MongoDB database, ensuring any existing `establishments` collection is dropped before the import.
- Import Necessary Libraries.
- Create MongoDB Client: An instance of the Mongo Client is created to connect to the MongoDB Atlas cluster.
- List Databases and Collections.
- Use `find_one()` and `pprint` to display a single document from the establishments collection.

## Part 2: Update the Database
- Insert the supplied data for the "Penang Flavours" restaurant into the `establishments` collection.
- Perform a query to find the `BusinessTypeID` for "Restaurant/Cafe/Canteen", and return only the `BusinessTypeID` and BusinessType fields.
- Update the "Penang Flavours" document with the correct `BusinessTypeID`.
- Perform a query to delete all documents in the collection where "Dover Local Authority" is the value for `LocalAuthorityName`. Perform a count before and after the deletion to ensure all documents were removed.
- Use the `update_many()` query to convert the `latitude` and `longitude` fields from strings to decimal numbers, and the `RatingValue` field to integers.

## Part 3: Exploratory Analysis
- Perform a query to find establishments with a hygiene score of 20. Use count_documents() to get the total number of matching documents, print the first result with pprint, and convert the results to a Pandas DataFrame to display the first 10 rows.
- Query for establishments in London with a RatingValue of 4 or higher using the $regex operator. Use count_documents() to get the total number of matches, print the first result with pprint, and convert the results to a Pandas DataFrame to display the first 10 rows.
- Query for establishments within 0.01 degrees of "Penang Flavours" with a RatingValue of 5, sorted by ascending hygiene score. Limit the results to 5, print them with pprint, and convert the results to a Pandas DataFrame to display.
- Create an aggregation pipeline to match documents with a hygiene score of 0, group by LocalAuthorityName and count the documents, and sort the counts in descending order. Send the pipeline to the aggregate() method, convert the results to a list, print the first ten with pprint, and convert the results to a Pandas DataFrame to display the first 10 rows.












