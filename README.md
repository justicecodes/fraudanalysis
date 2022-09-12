# project part 1 

## Topic: Credit Card Fraud Analysis

## Questions to answer: 
* Are there factors (gender, age, location, income range, time of day, category of purchase) that make you more susceptible to credit card fraud?

## Reasoning for topic choice: 
* 

## Dataset source:
* [Credit Card Transactions Fraud Detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection) dataset from Kaggle, training csv file is used for analysis
* [Average Income by US Zip Codes](https://www.kaggle.com/datasets/hamishgunasekara/average-income-per-zip-code-usa-2018?select=postcode_level_averages.csv) dataset from Kaggle

## Description of Communication Protocols: 
* Slack:
  * Daily casual communication in a group Slack channel to report progress of small group meetings and individual questions to collaborate on code
* Zoom:
  * Whole group meetings during class T/Th 7-9pm
  * M/W/Su group zoom meetings 9-10pm, some meetings are whole group, some are small groups within the team to collaborate on certain project segments
  * management of meeting times is communicated through Slack

## Machine Learning Model:
* We are using a supervised machine learning model to help determine if a credit card transaction is fraud or not fraud
* First, we are using feature importance/random forest to see which features are more predictive - age range, m/f
* Next, we are using a logistic regression model to classify if transactions in the training group are fraud or not fraud. The goal is that the model and accuracy is replicable with the test set.
* Provisional model (screenshot?)


* Segment 2 draft:
  * Description of data preprocessing: 
  * Description of feature engineering and the feature selection, including their decision- making process: 
  * Description of how data was split into training and testing sets: 
  * Explanation of model choice, including limitations and benefits: 
  * Explanation of changes in model choice (if changes occurred between the Segment 2 and Segment 3 deliverables): 
  * Description of how they have trained the model thus far, and any additional training that will take place: 
  * Description of current accuracy score: 

## Database Mockup:
![db_mockup](https://user-images.githubusercontent.com/103595718/188918466-19835ca6-ffc0-4491-ac88-ea08f7ec6103.png)

* columns/ features being used in each dataset
<img width="415" alt="zipcode_columns_touse" src="https://user-images.githubusercontent.com/103595718/188771476-225adb69-2565-4983-b024-f3d48e041b6a.png">
<img width="1227" alt="fraudTrain_columns_touse" src="https://user-images.githubusercontent.com/103595718/188771294-ecfe175c-8c25-42dc-8425-0ac6ea668b7c.png">

* ERD 
<img width="914" alt="Screen Shot 2022-09-05 at 9 42 24 PM" src="https://user-images.githubusercontent.com/103544626/189564354-b14de851-7160-4d84-ae77-9799c0cba3a4.png">

* create schema w sqlalchemy 
* add SQLlite file to connect machine learning file to data files

## Technologies used:
* Jupyter Notebook - dataframes, machine learning model
* PgAdmin (editing dataset to remove rows/columns)
* Tableau - pie chart of male vs female and category, bar chart of age ranges & income ranges, bar chart of time of day, map of location of card holders

## Roles:
(lead of each role, proposed roles) 
* Machine learning model - Lindsay, Dylan
* SQL / Postgres - Dhwani
* Tableau - Jenna
* Jupyter Notebook (summary stats) - Mustafa
* Square (github / project manager / slideshow presentation at end) - 

Original roles
* Square (git) - Jenna
* Triangle (machine learning) - Lindsay
* Circle (dataset) - Mustafa
* X Triangle (technologies used) - Dylan
* X Circle (technologies used) - Dhwani

