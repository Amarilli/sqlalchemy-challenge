# A climate analysis about  Honolulu, Hawaii

## Part 1: Analyze and Explore the Climate Data

I used Python and SQLAlchemy to do a basic climate analysis and data exploration of my climate database. Specifically, I used SQLAlchemy ORM queries, Pandas, and Matplotlib. To do so, I completed the following steps:

1. I used the provided files (`climate_starter.ipynb` and `hawaii.sqlite`) to complete my climate analysis and data exploration.

2. I used the SQLAlchemy `create_engine()` function to connect to my SQLite database.

3. I use the SQLAlchemy `automap_base()` function to reflect my tables into classes and then save references to the classes named station and measurement.

4. I linked Python to the database by creating a SQLAlchemy session.

5. I performed a **precipitation analysis** and then a **station analysis** by completing the steps in the following two subsections:

### Precipitation Analysis

- Find the most recent date in the dataset.

- Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.

- Select only the "date" and "prcp" values.

- Load the query results into a Pandas DataFrame. Explicitly set the column names.

- Sort the DataFrame values by "date".

- Plot the results by using the DataFrame plot method:

  ![line_plot](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/precipitation.png)

### Station Analysis

- I designed a query to calculate the total number of stations in the dataset.

- I found the most-active stations (that is, the stations that have the most rows)

- I designed a query that calculates the lowest, highest, and average temperatures that filter on the most active station ID found in the previous query.

- I designed a query to get the previous 12 months of temperature observation (TOBS) data 

- I created an histogram with bins=12 to display the results:

  ![histogram](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/tobs.png)

## Part 2: Design Your Climate App

I created a Flask API based on the queries I just developed using Flask to create the routes:

1. `/`

- Start at the homepage.

-List all the available routes.

![routes](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/routes.png)

2. `/api/v1.0/precipitation`

- Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.

- Return the JSON representation of your dictionary.

  ! [precipitations](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/precipitations.png)

3. `/api/v1.0/stations`

 - Return a JSON list of stations from the dataset.

   ![stations](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/stations.png)
   
4. `/api/v1.0/tobs`

- Query the dates and temperature observations of the most-active station for the previous year of data.

- Return a JSON list of temperature observations for the previous year.

  ![tobs_api](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/tobs_api.png)

5. `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`

- Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

  ![start and end](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/start_end_date.png)
 

- For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.

  ![start](https://github.com/Amarilli/sqlalchemy-challenge/blob/main/Resources/start_date.png)

