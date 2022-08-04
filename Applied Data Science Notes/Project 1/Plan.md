## Topic
- **An Analysis of Uber and Lyft Pricing Model Short Term and Long Term**
	- Does Uber offer a better deal than Yellow Taxi in general? if not in what case?
	- How does Uber determines its price.
	- ![EBITDA](https://www.gstatic.com/education/formulas2/443397389/en/ebitda_formula_ebitda_formula_var_1.svg)
	- VS Operating expenses


Earnings Before Interest, Taxes, Depreciation, and Amortization


## Doc
- PySpark Documentation: https://spark.apache.org/docs/latest/api/python/#:~:text=PySpark%20is%20an%20interface%20for,data%20in%20a%20distributed%20environment.



## Data collection
- https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- https://www1.nyc.gov/assets/tlc/downloads/pdf/trip_record_user_guide.pdf
- https://data.cityofnewyork.us/Transportation/Real-Time-Traffic-Speed-Data/qkm5-nuaq Real Time Traffic Speed Data
- https://data.cityofnewyork.us/browse?sortBy=most_accessed&utf8=%E2%9C%93
- https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95 Motor vehicle crashes

## Preprocessing 
- Use Data from 2019
- How to deal with bad/missing data
	- Removal
	- Potentially can take a look at the distribution of that specific feature, if the data seems to be together than we can replace missing data with mean. Else if the std is big we might have to remove that row.
- Watch out for an imbalance data set
	- This might just be the nature of the trips, will have to adjust K to account for this problem
- Has to discretise the data into different bins
	- Use KNN on the vectors of trips, to see if there are clear clusters. K need to be very large as sample size is huge. However we can take a smaller sample
	- If there are clusters, find out why this is the case
	- Here we are using the X and Y axis as features for KNN, can consider alternatives, but if we have too many features we might have to go with SVM.
- Find the average prize per minute per quarter for the period between Uber and Yellow Cab
	- Can account for seasonality
- Has to adjust for inflation and take into account economy of scale and economy of scope

## Feature Selection
- What is our model going to do?
	- Identify an overall trend for the prices of Uber and Yellow Taxi (Regression?)
	- Neural network to test the prediction ability, the prediction ability can be use as evaluation metric (more in the model section)
- Somehow fit a model and determine the features after?...
- What features to use for our model?
	- Forward/Backward stepwise selection? Potentially can use different methods Chi Squared, PMI or MI
	- Trial and error to find which set of features give the best evaluation score (optimisation)
- Potential features for the regression:
	- Since we are estimating a per minute pricing, we need to take into account the demand for uber rides within that given time interval. How do we determine that time interval? Average time to complete a trip?

## Model And Analysis (**at least 2 models**)
- Fit a Regression line
	- Are there confounding variables?
	- What does it look like?
- - Neural Network with Pytorch (https://www.youtube.com/watch?v=Jy4wM2X21u0)
- What is the evaluation metrics for the model?
- Want to have a model that would give an output such as number of trips in a day for either Uber and Lyft.

## Optimisation


## Discussion


