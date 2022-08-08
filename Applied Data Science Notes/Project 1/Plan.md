## Topic
- **An Analysis of Uber and Lyft tipping behaviour
	- Do customers tend to tip Uber and Lyft drivers?
	- When do they tip?
	- Why do they tip?
	- What are the things that effect the tipping? trip distance? arrival on time? weather? the location of tips? trip time?
	- Those who usually tip drivers, are they usually from the same area? pick up area? drop off area?
	- How much do they usually tip?
	- Can we predict the amount of a potential tip if it will happen?

## Doc
- PySpark Documentation: https://spark.apache.org/docs/latest/api/python/#:~:text=PySpark%20is%20an%20interface%20for,data%20in%20a%20distributed%20environment.



## Data collection
- https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- https://www1.nyc.gov/assets/tlc/downloads/pdf/trip_record_user_guide.pdf
- https://data.cityofnewyork.us/Transportation/Real-Time-Traffic-Speed-Data/qkm5-nuaq Real Time Traffic Speed Data
- https://data.cityofnewyork.us/browse?sortBy=most_accessed&utf8=%E2%9C%93
- https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95 Motor vehicle crashes

## Preprocessing 
- segregate Uber and Lyft data
- Make a new feature that is the time difference between request_datetime and onsceen_datetime
- group uber and Lyft data by regions and see if there are any tipping pattern
	- Which pickup location do people tip more? drop off?
	- Which region tend to tip more
- Aggregate data by miles to see the tipping pattern
- Aggregate data by time to see the tipping pattern
- Aggregate dataa by arrival time to see the tipping pattern
- Join with weather data to see if there are any tipping pattern base on weather

- Make correlation heat map to see what tipping is correlated to
- 

## Feature Selection
- select
	- trip miles
	- trip time
	- base_passenger_fare
	- driver pay
	- wav_request_flag
- 

## Model And Analysis (**at least 2 models**)
1. model to predict whether a customer will tip
2. model  to predict how much a customer will tip assumming they will tip

## Optimisation


## Discussion


