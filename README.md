# project part 1 

## Topic: Credit Card Fraud Analysis

## Questions to answer: 
* Are there factors (gender, age, location, income range, time of day, category of purchase) that make you more susceptible to credit card fraud?

## Dataset source:
[Credit Card Transactions Fraud Detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection) dataset from Kaggle
** Need another csv with at least one column same (zip code // avg income/race/FIPS score for that zip code) 

## Exploratory analysis ideas:


## Machine Learning Model Mockup:
* Our binary outcome variable is "is_fraud." It contains the categories Fraud and Not Fraud.
* We have run a logistic regression and a random forest classifier ML model to assist us in our understanding of who is likely to commit fraud. We are assessing the feature importance of the following variables to determine which are more predictive: AgeGroup, gender, city_pop, average_income, zip_code, and timeofday. 

## Description of data preprocessing
To preprocess our data for machine learning, we dropped the columns indicating the persons job (category), individuals' date of birth (dob), and the amount of money associated with the individuals' tracked transaction (amt). After that, we dropped all rows containing null value. Finally, we assigned numeric values to various strings in the df. The binary gender variables M or F became 1 or 2. The buckets created for AgeGroup and timeofday each recieved a numeric value of 1-5. 
 
 ✓ Description of how data was split into training and testing sets
 Data was split into a test set of 268,982 and a training set of 1,027,692, giving us roughly a 1:5 ratio.
 
 ✓ Explanation of model choice, including limitations and benefits
We selected a logistic regression because the appropriate dependent variable for assessment was "is fraud" or "is not fraud." To narrow our search into who commits fraud, we also performed a random forest feature selection. This gave the results below.

[(0.39983327283238834, 'time'),
 (0.14321961453874074, 'timeofday'),
 (0.113523267410041, 'city_pop'),
 (0.10888477241156184, 'avg_income'),
 (0.10725725402802479, 'zip'),
 (0.09435533192086078, 'age'),
 (0.01936477870215177, 'agegroup'),
 (0.01356170815623074, 'gender')]
 
 A limitation of our data is its simulated nature. It is unknown if our derived results are indiicative of real trends. 
 
 ✓ Explanation of changes in model choice (if changes occurred between the Segment 2 and Segment 3 deliverables)
 Given our high accuracy scores provided by both the logistic regression and the random forest, we did not alter our model choice. 
 
 ✓ Description of how they have trained the model thus far, and any additional training that will take place
 Our data contains roughly 1.3 million simulated credit card transactions. We could train this data further by creating a columns that attributes each zip code to a state or region, by adding  average income buckets, and reintegrating category into our analysis by grouping the jobs.  
 
 ✓ Description of current accuracy score
Our logistic regression provides an accuracy score of 0.9942226617394473
Our Random Forest Classifier provides an accuracy score of 8116594521290365

We could likely narrow the scope of our Random Forest Model further, in ways listed in the previous description of our training methods; however, both models are quite accurate at predicting who is likely to commit fraud. Considering that we are only planning to recommend fraud familiarization information to vulnerable groups, 81% would be considered a reliable accuracy score. 

## Database Mockup:
* create folder of csvs 
* columns/ features being used in each dataset*
* ERD (how dfs are being joined)
* Week 2 - upload into postgres (eventually join both tables)

## Technologies used:
* Jupyter Notebook - dataframes, machine learning model
* PgAdmin (editing dataset to remove rows/columns)
* Tableau - pie chart of male vs female and category, bar chart of age ranges & income ranges, bar chart of time of day, map of location of card holders

## Roles:
(lead of each role, proposed roles) 
* Machine learning model - 
* SQL / Postgres - 
* Tableau - 
* Jupyter Notebook (summary stats) - 
* Square (github / project manager / slideshow presentation at end) - 

Original roles
* Square (git) - 
* Triangle (machine learning) - 
* Circle (dataset) - 
* X Triangle (technologies used) - 
* X Circle (technologies used) - 

