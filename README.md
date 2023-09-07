# Module-12--nosql-challenge

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating.In this challenge  the editors of a food magazine, Eat Safe, Love, have assigned the task to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1: Database and Jupyter Notebook Set Up

1. Use NoSQL_setup_starter.ipynb for this section of the challenge.
2. Import the data provided in the establishments.json file from the Terminal.
3.  Name the database uk_food and the collection establishments.
4.  Copy the text used to import the data from the Terminal to a markdown cell in the notebook.
5.  Within the notebook, import the libraries needed: PyMongo and Pretty Print (pprint).
6.  Create an instance of the Mongo Client.
7.  Confirm that the database was created and the data properly loaded.
   
    * List the databases in MongoDB. Confirm that uk_food is listed.
    * List the collection(s) in the database to ensure that establishments is there.
    * Find and display one document in the establishments collection using find_one and display with pprint.
8.  Assign the establishments collection to a variable to prepare the collection for use.

## Part 2: Update the Database

Use NoSQL_setup_starter.ipynb for this section of the challenge.The magazine editors have some requested modifications for the database before performing any queries or analysis for them.
1. Make the following changes to the establishments collection:
    * An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet.
    * The magazine has asked it to be  include it in the analysis.
    *  Add the following information to the database:
     ![image](https://github.com/AsmaSaiyed/Module-12--nosql-challenge/assets/134350326/843ba477-0d1b-40cf-9a06-6bcf60d74715)
2. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
3. Update the new restaurant with the BusinessTypeID that was found.
4. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
5.  Some of the number values are stored as strings, when they should be stored as numbers.
     *  Use update_many to convert latitude and longitude to decimal numbers.
     *  Use update_many to convert RatingValue to integer numbers.

## Part 3: Exploratory Analysis
Eat Safe, Love has specific questions they want answered, which will help them find the locations they wish to visit and avoid.

Use NoSQL_analysis_starter.ipynb for this section of the challenge.Some notes to be aware of while exploring the dataset:
RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.

Use the following questions to explore the database, and find the answers, so a clear analysis can be provide to the magazine editors.
Some specefics for the analysis:
  * Unless otherwise stated, for each question:
  *  Use count_documents to display the number of documents contained in the result.
  *  Display the first document in the results using pprint.
  *  Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a RatingValue greater than or equal to 4?
   
3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.


