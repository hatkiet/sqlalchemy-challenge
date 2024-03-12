# sqlalchemy-challenge

**Instructions**

When planning a long vacation in Honolulu, Hawaii, it's important to analyze the climate of the area. The following sections outline the steps needed to accomplish this task.

**Part 1: Analyze and Explore the Climate Data**

To perform a basic climate analysis and data exploration of your climate database, you will need to use Python and SQLAlchemy. Specifically, you will use SQLAlchemy ORM queries, Pandas, and Matplotlib. Follow these steps to complete the process:

1. Use the provided files (climate_starter.ipynb and hawaii.sqlite) to conduct your climate analysis and data exploration.

2. Connect to your SQLite database using the SQLAlchemy create_engine() function.

3. Use the SQLAlchemy automap_base() function to reflect tables into classes. Then, save references to the classes named station and measurement.

4. Create a SQLAlchemy session to link Python to the database.

5. Conduct a precipitation analysis and a station analysis by following the steps in the two subsections provided.

Precipitation Analysis

The following analyses were conducted:

1. Determined the most recent date in the dataset.

2. Used the most recent date to extract the previous 12 months of precipitation data by querying the data.

3. Selected only the "date" and "prcp" values.

4. Loaded the query results into a Pandas DataFrame and set the column names explicitly.

5. Sorted the DataFrame values by "date".

6. Plotted the results using the DataFrame plot method.

<img width="907" alt="Screenshot 2024-03-12 at 5 22 50 PM" src="https://github.com/hatkiet/sqlalchemy-challenge/assets/154276115/a7a3358e-31dd-4e68-a486-cd7fbf3bae3a">

7. Used Pandas to print the summary statistics for the precipitation data.

<img width="210" alt="Screenshot 2024-03-12 at 5 23 06 PM" src="https://github.com/hatkiet/sqlalchemy-challenge/assets/154276115/86d26fef-040c-48ac-b711-573c8e7481c6">


Station Analysis

1. Designed a query to calculate the total number of stations in the dataset.

2. Designed a query to find the most-active stations (that is, the stations that have the most rows). List the stations and observation counts in descending order, and then find the station id that has the greatest number of observations

3. Designed a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.

4. Designed a query to get the previous 12 months of temperature observation (TOBS) data. 

- Filtered by the station that has the greatest number of observations.
- Queried the previous 12 months of TOBS data for that station.
- Plotted the results as a histogram with bins=12.

<img width="905" alt="Screenshot 2024-03-12 at 5 23 18 PM" src="https://github.com/hatkiet/sqlalchemy-challenge/assets/154276115/5811a7f9-e679-4d30-a974-e4717e8a8651">


5. Closed the session.

**Part 2: Design the Climate App**

1. Start at the homepage.

    List all the available routes.

2. /api/v1.0/precipitation

    Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value. And then return the JSON representation of your dictionary.

3. /api/v1.0/stations

    Return a JSON list of stations from the dataset.

4. /api/v1.0/tobs

   Query the dates and temperature observations of the most-active station for the previous year of data. And then return a JSON list of temperature observations for the previous year.

5. /api/v1.0/<start> and /api/v1.0/<start>/<end>

- Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

- For a specified start (in format YYYY-MM-DD), calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.

- For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.

[Note] I've used the knowledge and activities in class, especially, Week 10-Advanced-SQL, Day 3's activites to finish this challenge. I also used ChatGPT for finding bugs (if have)

