# Movies_ETL

## Project Overview 
Amazing Prime is sponsoring a hackathon that will provide a clean database of movie data and will ask the participants to predict popular movies. This project involved creating a clean database of movie data. The two data sources for this dataset are a scrap of Wikipedia for all movies released since 1990 and rating data from the MovieLens website. To complete this project, the data was extracted from the two sources, transformed, and then loaded into PostgreSQL. After that was completed, Amazing Prime asked for an automated pipeline that can take in new data, perform the transformations, and can load it into existing tables. 

## Resources
- Data: wikipedia-movies.json, movies_metadata.csv, and ratings.csv
- Python 3.7.11,Jupyter Notebook, PostGreSQL, 

## Results

### Deliverable 1 - Write an ETL Function to Read Three Data Files

A function was created to read the three data files and to create a path to the three data sources. Three data frames - one for each data source - were created. 

Wiki Movies DataFrame (data source: wikipedia-movies.json)

<img width="1006" alt="Screen Shot 2022-06-08 at 5 49 13 PM" src="https://user-images.githubusercontent.com/103774401/172741616-a247b063-1ae9-4fb8-89ab-9f3c851088dd.png">

Kaggle Metadata DataFrame (data source: movies_metadata.csv)

<img width="1006" alt="Screen Shot 2022-06-08 at 5 49 33 PM" src="https://user-images.githubusercontent.com/103774401/172741628-ee71a77d-0f64-45c9-a8dc-260fecca070f.png">

Ratings DataFrame (data source: ratings.csv)

<img width="326" alt="Screen Shot 2022-06-08 at 5 50 00 PM" src="https://user-images.githubusercontent.com/103774401/172741591-e49cc75c-600d-4371-abe4-c6472d27f3a5.png">

### Deliverable 2 - Extract and Transform the Wikipedia Data

The wikipedia data was transformed to merge it with the Kaggle metadata. This process included filtering out tv shows, converting values, changing column names, and cleaning columns after converting values. 

Cleaned Wiki Movies DataFrame

<img width="1049" alt="Screen Shot 2022-06-08 at 5 45 46 PM" src="https://user-images.githubusercontent.com/103774401/172741425-698e3e9e-5322-4ff3-b7de-6c9b7aa07fd4.png">

List of Wiki Movies DataFrame Columns

<img width="241" alt="Screen Shot 2022-06-08 at 5 46 42 PM" src="https://user-images.githubusercontent.com/103774401/172741439-29e95043-3286-4f16-aaa2-86d8382c3845.png">


### Deliverable 3 - Extract and Transform the Kaggle Data

Both the Kaggle Metadata and the ratings data were transformed and then converted into two separate DataFrames. Then, the Wiki Movies DataFrame and the cleaned Kaggle Metadata DataFrame were merged into a new Movies DataFrame. Finally, the cleaned Ratings DataFrame was merged with the Movies DataFrame. 

Movies with Ratings DataFrame

<img width="1011" alt="Screen Shot 2022-06-08 at 5 48 17 PM" src="https://user-images.githubusercontent.com/103774401/172741520-57d1f071-58d5-447d-93e4-2b5db6e8c6f4.png">

Movies DataFrame

<img width="1010" alt="Screen Shot 2022-06-08 at 5 48 39 PM" src="https://user-images.githubusercontent.com/103774401/172741557-c83d26e4-cbee-4337-b760-7a5e7ccda2a9.png">


### Deliverable 4 - Create the Movie Database

A new database was created in PostgreSQL that contains both the Movies Dataframe and the Ratings DataFrame.

Creating Database Code

<img width="900" alt="Screen Shot 2022-06-08 at 5 45 03 PM" src="https://user-images.githubusercontent.com/103774401/172741317-acf0e040-a4fe-4b4a-b520-30374ff341fc.png">

Movies Query

<img width="735" alt="movies_query" src="https://user-images.githubusercontent.com/103774401/172741337-29b50606-dfaf-4404-9746-8b49d3909282.png">

Ratings Query

<img width="735" alt="ratings_query" src="https://user-images.githubusercontent.com/103774401/172741356-253b72cc-0fa2-471a-adc9-2836c5a22746.png">

## Summary
The database for Amazing Prime's Hackathon was created successfully by extracting, transforming, and loading the movie data
