# Identifying Important Factors Affecting an Individual's Income
Creating and Analyzing Visualizations based on Income data

## Summary
* [Introduction & General Information](#introduction--general-information)
* [Objectives](#objectives)
* [Data Used](#data-used)
* [Approach & Methodology](#approach--methodology)
* [Run Locally](#run-locally)
* [Conclusion](#conclusion)

## Introduction & General Information
- A certain corporation is using the income data supplied by the United States Census Bureau to develop the marketing profiles of people. The role of the corporation is to help universities to develop marketing strategies for their degree programs in a manner to boost their enrolments.
- There are many factors affecting the individual's income like age, gender, education status, marital status, occupation etc.
- The data analysts of the corporation will analyze these factors and develop strategies to target certain group of people. For the purpose of this project, $50k has been considered the key income for analyzing these factors.

## Objectives
- Creating useful visualization based on the census income data and analyzing these visualizations to identify the most important factors contributing to an individual’s income.

## Data Used
(Data Source: https://archive.ics.uci.edu/ml/machine-learning-databases/adult/)
- This data has been extracted from the [census bureau database](http://www.census.gov/ftp/pub/DES/www/welcome.html).
- The database consists of 14 attributes such as age, gender, education status, marital status, occupation etc. which may affect the individual's income.
- The entire database is divided in two class labels - >50K and <=50K income group.

## Approach & Methodology
- Convert the given dataset into pandas dataframe and then clean the dataframe to remove the missing values.
- Create and Analyze Bivariate Visualizations of each of the 14 attributes against the class label, Salary using various visualization techniques.
- Identify useful attributes for income prediction.
- Create and Analyze Multivariate Visualizations of the useful attributes identified above.

## Run Locally
* Make sure Python 3 is installed. Reference to install: [Download and Install Python 3](https://www.python.org/downloads/)
* Clone the project: `git clone https://github.com/setu-parekh/income-prediction-factors-indentification.git`
* Route to the cloned project: `cd income-prediction-factors-indentification`
* Install necessary packages: `pip install -r requirements.txt`
* Run Jupyter Notebook: `jupyter notebook`
* Select the notebook to open: `factors_identification_by_visualization.ipynb`

## Conclusion
* Following factors have been identified to play important role in predicting individual's income:
  * **Age**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/age_distribution.png), it can be be observed that there are greater chances of people in the age between 40 - 50 years earning more than 50K income.
    - Those in the age group of 15-20, 70-90 years have very little chance of earning greater than 50K.
  * **Education**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/education_distribution.png), it can be observed that most of the people in this dataset have only high school as their highest level of education. Only small portion are having doctoral degrees.
    - Low income category mostly comprises of those people with their highest education as High School graduate, Bachelors and college graduate and others who are not even high school graduate.
    - Only those with masters and doctoral degree are earning greater than 50K income.
  * **Marital Status**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/marital_status_distribution.png), it can be observed that all categories except Married-civ-spouse are clearly weighted towards  less than 50K income.
    - The income distribution in Married-civ-spouse category is almost equally distributed.
  * **Occupation**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/occupation_distribution.png), it can be observed that people with executive-managerial and Prof-speciality roles are earning more than 50K income due to their higher rank of occupation.
    - Remaining all occupation groups are most likely to have income lower than 50K.
  * **Relationship**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/relationship_distribution.png), it can be observed that all categories except husband and wife are earning less than 50K.
    - However, probability of husband and wife falling in either class is almost similar.
  * **Capital Gain**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/capital_gain_distribution.png), it can be observed that majority of the data lies near 0 capital gain.
    - Capital gain is widely distributed for people earning greater than 50K as compared to those earning less than 50K.
    - So, if a person is having higher capital gain, it is more likely that they will fall under greater than 50K category.
  * **Hours per Week**:
    - From the [visualization](https://github.com/setu-parekh/income-prediction-factors-indentification/blob/main/graphs/hours_per_week_distribution.png), it can be observed that average working hours for the entire dataset is 40 hrs.
    - Those working fewer than 40 hrs are earning less than 50K.
    - There are greater chances of people working more than 40 hrs earning higher than 50K.

* Hence, people with lower income can easily be identified from above factors and targeted for marketing of degree courses.





