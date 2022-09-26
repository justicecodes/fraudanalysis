## Project: Part 1

## Topic: Credit Card Fraud Analysis

## Link to Presentation

## Reasoning for Topic Choice:
* Credit card usage has been increasing steadily over the years, but even moreso with change shortages and COVID in the past few years. 28% of all transactions are with credit cards as of 2021. 80% of American adults have had a credit card account, with an average of 3 cards per person. With the increased usage, credit card fraud is also becomming more prevalent. We agreed that everyone has had to deal with recouperating fraudulent charges or know someone close to them who has. Our project group is interested in finding out if there are patterns or basic personal information (age, location, time of day) that makes people more susceptible to credit card fraud. The data we are using is limited in that it does not disclose how the credit card was used, for example if the card was physically stolen, entered online through phishing schemes, or any other method. Other uncertainties with results may occur with simulated data fields due to personal privacy laws. Models and results visualized as graphs will focus on personal demographics that may make a person more susceptible to fraud so that our audience may have a better idea how to keep their credit card usage safer overall.

## Dataset Source:
* [Credit Card Transactions Fraud Detection dataset from Kaggle](https://www.kaggle.com/datasets/kartik2112/fraud-detection)
* [Average Income by US Zip Codes dataset from Kaggle](https://github.com/justicecodes/projectpractice#dataset-source:~:text=Average%20Income%20by%20US%20Zip%20Codes) 

## Database Mockup

<img width="605" alt="Screen Shot 2022-09-19 at 2 31 53 AM" src="https://user-images.githubusercontent.com/104036750/190969448-002e13ff-b88a-4b93-8c6c-ae0321d3e486.png">


<img width="422" alt="Screen Shot 2022-09-19 at 2 31 57 AM" src="https://user-images.githubusercontent.com/104036750/190969459-b04d7773-e766-4006-b77e-5ace15667650.png">



<img width="615" alt="Screen Shot 2022-09-19 at 2 32 02 AM" src="https://user-images.githubusercontent.com/104036750/190969462-672408bf-c9b1-42d8-992c-404c5264b015.png">






## Description of Communication Protocols:
* Slack:
  * Daily casual communication in a group Slack channel to report progress of small group meetings and individual questions to collaborate on code
* Zoom:
  * Whole group meetings during class T/Th 7-9pm
  * M/W/Su group zoom meetings 9-10pm, some meetings are whole group, some are small groups within the team to collaborate on certain project segments
management of meeting times is communicated through Slack

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
    
## Technologies:
* Jupyter Notebook - dataframes, machine learning model
* PgAdmin (editing dataset to remove rows/columns)
* Tableau - pie chart of male vs female and category, bar chart of age ranges & income ranges, bar chart of time of day, map of location of card holders

## Roles:
Proposed Roles:
* Machine learning model - Lindsay, Dylan
* SQL / Postgres - Dhwani
* Tableau - Jenna
* Jupyter Notebook (summary stats) - Mustafa
* Square (github / project manager / slideshow presentation at end) -

Original Roles:
* Square (git) - Jenna
* Triangle (machine learning) - Lindsay
* Circle (dataset) - Mustafa
* X Triangle (technologies used) - Dylan
* X Circle (technologies used) - Dhwani

## Tableau Graphs

Fraud/Gender Pie Chart


<img width="854" alt="Screen Shot 2022-09-25 at 11 17 55 PM" src="https://user-images.githubusercontent.com/104036750/192193399-2ba0a056-0b18-48e4-b29f-c31cb629e0b8.png">


Fraud/Time of Day Pie Chart


<img width="863" alt="Screen Shot 2022-09-25 at 11 18 06 PM" src="https://user-images.githubusercontent.com/104036750/192193411-0d2f6a21-82a4-4682-ac5b-8854b7551b4d.png">


Fraud Count/Age Group Bar Graph


<img width="856" alt="Screen Shot 2022-09-25 at 11 18 25 PM" src="https://user-images.githubusercontent.com/104036750/192193454-b38ab08c-9f7d-4828-bcf4-ebc0a42d110e.png">


Fraud Count Bar Graph


<img width="430" alt="Screen Shot 2022-09-25 at 11 18 42 PM" src="https://user-images.githubusercontent.com/104036750/192193460-5417036e-ffef-4680-a1f3-bca8100fbb10.png">


Fraud Amount Bar Graph


<img width="436" alt="Screen Shot 2022-09-25 at 11 18 53 PM" src="https://user-images.githubusercontent.com/104036750/192193502-5199588b-50f8-441a-bb8d-26ea21b34255.png">


Fraud Amount/Category Bar Graph


<img width="648" alt="Screen Shot 2022-09-25 at 11 19 02 PM" src="https://user-images.githubusercontent.com/104036750/192193507-15d0bcd0-3ff8-4bd6-9f92-3713fcc41768.png">



