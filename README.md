# Starbucks Capstone Challenge
## Getting Started
### Installation

- Python 3.6
- NumPy
- Pandas (update you pandas to be able to read in the json files correctly)
- Math
- Machine Learning libraries such as Scikit-Learn model: LogisticRegression, RandomForestClassifier  and other Scikit-Learn components
- XGBoost
- Visualization packages such as Seaborn and matplotlib
- Regular expression operation python package such as re
- Json

 ## Project Overview  
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

Your task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.

You'll be given transactional data showing user purchases made on the app including the timestamp of purchase and the amount of money spent on a purchase. This transactional data also has a record for each offer that a user receives as well as a record for when a user actually views the offer. There are also records for when a user completes an offer.

Keep in mind as well that someone using the app might make a purchase through the app without having received an offer or seen an offer.

## Project Motivation
In this project, we will be answering the following business questions:<br>
1) Determine which demographic groups, i.e.age, gender and income groups, respond best to the offer types<br>
2) Assess characteristics of the demographic groups who respond the least to offers<br>
3) Build a model to predict what features affect a user's response to an offer<br>

## Project Components
### Project Details 
The data is contained in three files:

-portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)<br>
-profile.json - demographic data for each customer<br>
-transcript.json - records for transactions, offers received, offers viewed, and offers completed<br>

Here is the schema and explanation of each variable in the files:

**portfolio.json**

-id (string) - offer id<br>
-offer_type (string) - type of offer ie BOGO, discount, informational<br>
-difficulty (int) - minimum required spend to complete an offer<br>
-reward (int) - reward given for completing an offer<br>
-duration (int) - time for offer to be open, in days<br>
-channels (list of strings)<br>

**profile.json**

-age (int) - age of the customer<br>
-became_member_on (int) - date when customer created an app account<br>
-gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)<br>
-id (str) - customer id<br>
-income (float) - customer's income<br>

**transcript.json**

-event (str) - record description (ie transaction, offer received, offer viewed, etc.)<br>
-person (str) - customer id<br>
-time (int) - time in hours since start of test. The data begins at time t=0<br>
-value - (dict of strings) - either an offer id or transaction amount depending on the record<br>

### File Description
- Data zip folder contains the three datasets listed above<br>
- Models folder contains the trained models in this project<br>
- Notebook contains the python code used to execute this project<br>

## Summary of the results
In summary, here are the insights from the data which answers to the business questions:-

- The 40-60 age range, Male, and the 40-60K income range respond best to offers<br>
- BOGO was the most significant offer type that determined the success of an offer<br>
- The total amount of a transaction plays a key role in determining whether a customer responds to an offer or not<br>
- Social media was the most significant channel that determined the success of an offer<br>
- The minimum required spend to complete an offer and membership days also determines the success of an offer<br>
- The <20 age range, Female and the 100+K income range respond the least to offers<br>

##  Acknowledgements
This project was completed by me as part of the Udacity Data Scientist Nanodegree. Code templates and training were provided by Udacity. The data was originally sourced by Udacity from Starbucks. For more details about this project, visit [my blog post.](https://medium.com/@thanksgivingtogod94/how-can-starbucks-determine-the-effectiveness-of-their-campaign-offers-bb3e0375833e)
