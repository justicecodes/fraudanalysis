
# Credit Card Fraud Analysis

## [Link to Presentation](https://docs.google.com/presentation/d/1-1RvOME2adhu_sqhdcV004dQU8e36NeqqYgtGavd53A/edit?usp=sharing)

## Questions to answer: 
* Are there factors (gender, age, location, income range, time of day, category of purchase) that make you more susceptible to credit card fraud?

## Reasoning for topic choice: 
* Credit card usage has been increasing steadily over the years, but even moreso with change shortages and COVID in the past few years. 28% of all transactions are with credit cards as of 2021. 80% of American adults have had a credit card account, with an average of 3 cards per person. With the increased usage, credit card fraud is also becomming more prevalent. We agreed that everyone has had to deal with recouperating fraudulent charges or know someone close to them who has.  Our project group is interested in finding out if there are patterns or basic personal information (age, location, time of day) that makes people more susceptible to credit card fraud. The data we are using is limited in that it does not disclose how the credit card was used, for example if the card was physically stolen, entered online through phishing schemes, or any other method. Other uncertainties with results may occur with simulated data fields due to personal privacy laws. Models and results visualized as graphs will focus on personal demographics that may make a person more susceptible to fraud so that our audience may have a better idea how to keep their credit card usage safer overall.  [Source](https://www.forbes.com/advisor/credit-cards/credit-card-statistics/)

## Cohesive, structured outline of the project (this may include images, but they should be easy to follow and digest)

## Dataset source:
* [Credit Card Transactions Fraud Detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection) dataset from Kaggle, training csv file is used for analysis
* [Average Income by US Zip Codes](https://www.kaggle.com/datasets/hamishgunasekara/average-income-per-zip-code-usa-2018?select=postcode_level_averages.csv) dataset from Kaggle

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
<img width="921" alt="Final ERD Diagram" src="https://user-images.githubusercontent.com/103150314/189564519-ad4a322e-b1af-4c75-90fb-cc263ddbb9c8.png">

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

