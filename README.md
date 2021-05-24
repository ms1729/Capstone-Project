# Capstone-Project
## DSND-Blog-Post

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

The relevant Python packages for this project are as follows:

- pandas
- numpy
- math
- json
- matplotlib
- seaborn

## Project Motivation<a name="motivation"></a>

This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer, and that was the challenge to solve with this data set. Our task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

The data is contained in three files:

- portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
- profile.json - demographic data for each customer
- transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

portfolio.json

- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

profile.json

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

transcript.json

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

Here are the questions I would like to answer --

- What is the best offer for the overall target audience?
- What is/are the best offer(s) at an individual personalized level?
- - Based on Age
- - Based on Income
- - Based on Gender & Age
- - Based on Gender & Income
- Where do we have the opportunity to increase the number of offers being sent for certain demographics to increase sales?
- How much reward was given to individuals that did not view the offers sent to them?

There are three types of offers that are being sent:

- Buy-One-Get-One (BOGO),
- Discount, and
- Informational

For each of these offer types they further have subtypes. My focus in analyzing the datasets and trying to answer these questions would focus on BOGO and Discount types.


## File Descriptions <a name="files"></a>

There is 1 notebook available here to showcase work related to the above questions.  The notebook is exploratory in searching through the data pertaining to the questions showcased by the notebook title.

## Results<a name="results"></a>

The main findings of the code can be found at the post available [here](https://mohitsharma13.medium.com/capstone-challenge-starbucks-offers-cb35a44ed57a).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Feel free to use the code here as you would like! 

