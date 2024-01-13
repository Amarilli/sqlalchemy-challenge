# sqlalchemy-challenge

## A climate analysis about  Honolulu, Hawaii.

### Part 1: Analyze and Explore the Climate Data

I used Python and SQLAlchemy to do a basic climate analysis and data exploration of my climate database. Specifically, I used SQLAlchemy ORM queries, Pandas, and Matplotlib. To do so, I completed the following steps:

1. I used the provided files (`climate_starter.ipynb` and `hawaii.sqlite`) to complete my climate analysis and data exploration.

2. I used the SQLAlchemy `create_engine()` function to connect to my SQLite database.

3. I use the SQLAlchemy `automap_base()` function to reflect my tables into classes, and then save references to the classes named station and measurement.

4. I linked Python to the database by creating a SQLAlchemy session.

5. I performed a **precipitation analysis** and then a **station analysis** by completing the steps in the following two subsections:

#### Precipitation Analysis

- Find the most recent date in the dataset.

- Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.

- Select only the "date" and "prcp" values.

- Load the query results into a Pandas DataFrame. Explicitly set the column names.

- Sort the DataFrame values by "date".

- Plot the results by using the DataFrame plot method:

#### Station Analysis



