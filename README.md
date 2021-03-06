# SQLAlchemy - Surfs Up!



## Step 1 - Climate Analysis and Exploration

I used Python and SQLAlchemy to do basic climate analysis and data exploration of your climate database. All of the analysis was completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.


### Precipitation Analysis

* I designed a query to retrieve the last 12 months of precipitation data, selecting only the `date` and `prcp` values.

* The query results were loaded into a Pandas DataFrame and the index was set to the date column.

* The DataFrame values were sorted by `date`.

* The results were plotted using the DataFrame `plot` method.

  ![precipitation](Images/precipitation.png)

### Station Analysis

* I designed queries calculating the total number of stations, the most active stations(most observations), and retrieving the last 12 months of temperature observation data.

* The results were plotted as a histogram.

    ![station-histogram](Images/station-histogram.png)

- - -

## Step 2 - Climate App

I designed a Flask API based on the queries I developed in the earlier steps, using Flask to create my routes and 'jsonify' to to convert my API data into a valid JSON response object. 

### Routes

* `/`

  * Home page.

* `/api/v1.0/precipitation`

* `/api/v1.0/stations`

* `/api/v1.0/tobs`

* `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`

  * A JSON list of the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.

  * When given the start only, calculate `TMIN`, `TAVG`, and `TMAX` for all dates greater than and equal to the start date.

  * When given the start and the end date, calculate the `TMIN`, `TAVG`, and `TMAX` for dates between the start and end date inclusive.

- - -

### Optional: Other Recommended Analyses

### Temperature Analysis I

* Identify the average temperature in June at all stations across all available years in the dataset. Do the same for December temperature.

* Use the t-test to determine whether the difference in the means, if any, is statistically significant. Will you use a paired t-test, or an unpaired t-test? Why?

### Temperature Analysis II

* Use the `calc_temps` function to calculate the min, avg, and max temperatures for your trip using the matching dates from the previous year (i.e., use "2017-01-01" if your trip start date was "2018-01-01").


    ![temperature](Images/temperature.png)

### Daily Rainfall Average

* Calculate the rainfall per weather station using the previous year's matching dates.

* Calculate the daily normals. Normals are the averages for the min, avg, and max temperatures.


  ![daily-normals](Images/daily-normals.png)

