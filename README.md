
# Credit Card Fraud Analysis

## [Link to Presentation](https://docs.google.com/presentation/d/1-1RvOME2adhu_sqhdcV004dQU8e36NeqqYgtGavd53A/edit?usp=sharing)
## [Link to Dashboard](https://public.tableau.com/app/profile/dylan.jungmann/viz/Project_16638840211390/Story2?publish=yes)

## Focus Question: 
* Are there factors (gender, age, location, income range, time of day, category of purchase) that make you more susceptible to credit card fraud?

## Reasoning for topic choice: 
* Credit card usage has been increasing steadily over the years, but even moreso with change shortages and COVID in the past few years. 
* 28% of all transactions are with credit cards as of 2021. 
* 80% of American adults have had a credit card account, with an average of 3 cards per person. 
* With the increased usage, credit card fraud is also becomming more prevalent. We agreed that everyone has had to deal with recouperating fraudulent charges or know someone close to them who has.  
* Our project group is interested in finding out if there are patterns or basic personal information (age, location, time of day) that makes people more susceptible to credit card fraud. 
* The data we are using is limited in that it does not disclose how the credit card was used, for example if the card was physically stolen, entered online through phishing schemes, or any other method. Other uncertainties with results may occur with simulated data fields due to personal privacy laws.
* Models and results visualized as graphs will focus on personal demographics that may make a person more susceptible to fraud so that our audience may have a better idea how to keep their credit card usage safer overall.  [Source](https://www.forbes.com/advisor/credit-cards/credit-card-statistics/)

## Project Outline:
1. ETL 
  * Original CSVs were read into a Jupyter Notebook file. Unnecessary columns were deleted from both csv files.  New columns were created to extract the age from DOB (then age group buckets) and time from UNIX time (then time-of-day buckets). Dollar signs were added and decimal points rounded on columns relating to money.
  * NaN and duplicate rows deleted
2. SQL
  * Cleaned CSVs uploaded and merged into one table
  * Additional tables created to show only fraudulent charges and other tables for visualizations
3. Machine Learning
  * New Dataset loaded into Machine Learning model using SQLAlchemy 
  * Processed using Logistic Regression & Balance Random Forest for final analysis
4. Dashboard
  * Tableau used for storyboards
  * Confirmed by summary statistics, using Pandas
  * Machine Learning confusion matrix

## Dataset source:
* [Credit Card Transactions Fraud Detection](https://www.kaggle.com/datasets/kartik2112/fraud-detection) dataset from Kaggle, training csv file is used for analysis
* [Average Income by US Zip Codes](https://www.kaggle.com/datasets/hamishgunasekara/average-income-per-zip-code-usa-2018?select=postcode_level_averages.csv) dataset from Kaggle

## Machine Learning Model:
* Our binary outcome variable is "is_fraud." It contains the categories Fraud and Not Fraud.
* We have run a logistic regression and a random forest classifier ML model to assist us in our understanding of who is likely to commit fraud. We are assessing the feature importance of the following variables to determine which are more predictive: AgeGroup, gender, city_pop, average_income, zip_code, and timeofday.
* Given our high accuracy scores provided by both the logistic regression and the random forest, we did not alter our model choice throughout the project

### Description of data preprocessing:
* To preprocess our data for machine learning, we dropped the columns indicating the persons job (category), individuals' date of birth (dob), and the amount of money associated with the individuals' tracked transaction (amt). After that, we dropped all rows containing null values. Finally, we assigned numeric values to various strings in the df. The binary gender variables M or F became 1 or 2. The buckets created for AgeGroup and timeofday each recieved a numeric value of 1-5.
* Data was split into a test set of 268,982 and a training set of 1,027,692, giving us roughly a 1:5 ratio. As can be seen in the image below, we used counter to deliniate the number of fraudulent cases analyzed versis not fraud cases. 

![split.png](/mlvisualizations/split.png)
### Results: 
In our initial machine learning file (merged data ML model), we attempted to resolve issues associated with the sampling size by oversampling and undersampling. However, both of these solutions reduced our accuracy score and provided more errors. It is likely that these issues arose due to the covariance within our independent variables. Some of the errors can be seen in our confusion matrix and logistic regression classification. 

![LOGconfusion.png](/mlvisualizations/LOGconfusion.png)
![LOGclassification.png](/mlvisualizations/LOGclassification.png)

Other errors we attempted to troubleshoot in our machine learning were found within the random forest classifier. Our final feature selection analysis only included those shown in the image below. But, when time of day was included in our analysis our accuracy score improved to 81%. We decided to remove this feature because additional information would need to be provided about the data collection. 

![sorted features.png](/mlvisualizations/sorted features.png)

✓ Description of current accuracy score Our logistic regression provides an accuracy score of 0.9942226617394473 Our Random Forest Classifier provides an accuracy score of 0.6648701908753212

![LOGaccuracy.png](/mlvisualizations/LOGaccuracy.png)
![RFCaccuracy.png](/mlvisualizations/RFCaccuracy.png)

### Limitations or suggestions for future analysis: 
  * A limitation of our data is its simulated nature. It is unknown if our derived results are indiicative of real trends.
  * We could train this data further by creating a columns that attributes each zip code to a state or region, by adding average income buckets, and reintegrating category into our analysis by grouping the jobs.
  * We could likely narrow the scope of our Random Forest Model further, in ways listed in the previous description of our training methods. If we could determine that the fraudulent purchases' time of day could be tied to typical patterns of that person, then the RFC would be accurate enough to utilize as a tool that predicts someone's propensity to commit fraud or not. 

## Database:
![db_mockup](https://user-images.githubusercontent.com/103595718/188918466-19835ca6-ffc0-4491-ac88-ea08f7ec6103.png)
* ERD 
<img width="921" alt="Final ERD Diagram" src="https://user-images.githubusercontent.com/103150314/189564519-ad4a322e-b1af-4c75-90fb-cc263ddbb9c8.png">

## Technologies used:
* Jupyter Notebook - dataframes, machine learning model
* PgAdmin (editing dataset to remove rows/columns)
* Tableau - pie chart of male vs female and category, bar chart of age ranges & income ranges, bar chart of time of day, map of location of card holders

## Roles: 
* Square (git and presentation) - Jenna
* Triangle (machine learning) - Lindsey
* Circle (dataset) - Dhwani & Mustafa
* Dashboard (tableau) - Dylan

