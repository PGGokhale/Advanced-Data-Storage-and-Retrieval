# SQLAlchemy_Flask-Homework
This repository contains the homework for SQLAlchemy and Flask of Data Analysis and Visualization Bootcamp Nov 2019-May 2020

This homework contains two parts.

## Step 1 - Climate Analysis and Exploration

This part of the work is done in the Honolulu_climate_analysis.ipynb jupyter notebook.
Python and SQLAlchemy is used to do basic climate analysis and data exploration climate database. All of the analysis is completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.
### Precipitation Analysis
* A query is designed to retrieve the last 12 months of precipitation data and created a plot for the same

### Station Analysis
* A query is designed to calculate the total number of stations.

* A query is designed to find the most active stations.
* A query is designed to retrieve the last 12 months of temperature observation data (tobs) of the most active station and generated a histogram for the same.


## Step 2 - Climate App

After completing the initial analysis, a Flask API is designed based on the queries that are developed.
This is done in MyClimateApp.py

### Routes
Following routes are available in the Flask API
* `/`

  * Home page.

  * Lists all routes that are available.

* `/api/v1.0/precipitation`

  * Converts the query results to a Dictionary using `date` as the key and `prcp` as the value.

  * Return the JSON representation of your dictionary.

* `/api/v1.0/stations`

  * Return a JSON list of stations from the dataset.

* `/api/v1.0/tobs`
  * query for the dates and temperature observations from a year from the last data point.
  * Return a JSON list of Temperature Observations (tobs) for the previous year.

* `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`

  * Return a JSON list of the minimum temperature, the average temperature, and the max temperature for a given start or start-end range.

  * When given the start only, calculate `TMIN`, `TAVG`, and `TMAX` for all dates greater than and equal to the start date.

  * When given the start and the end date, calculate the `TMIN`, `TAVG`, and `TMAX` for dates between the start and end date inclusive.

