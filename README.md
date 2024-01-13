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

### Part 2: Design Your Climate App

Now that you’ve completed your initial analysis, you’ll design a Flask API based on the queries you just developed. To do so, use Flask to create your routes as follows:

1. /

- Start at the homepage.

-List all the available routes.

2. `/api/v1.0/precipitation`

- Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.

- Return the JSON representation of your dictionary.

3. `/api/v1.0/stations`

 - Return a JSON list of stations from the dataset.
   
4. `/api/v1.0/tobs`

- Query the dates and temperature observations of the most-active station for the previous year of data.

- Return a JSON list of temperature observations for the previous year.

5. `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`

- Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

- For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.



