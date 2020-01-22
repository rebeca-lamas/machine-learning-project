# Machine Learning Project
This project use machine learning to predict the box office success of movies.

## Driving Questions
1.  Can machine learning predict the box office for a movie being released next year? (Multiple linear regression)
2.  Can machine learning predict if a movie will be in the top 20 for the year? (Logistical Regression)

## Extracting and Transforming Data
* Used pandas, and beautiful soup to web scraping creating comprehensive lists of movies released each year.
* Compiled data through API calls to the OMDb API.
* Data was cleaned and transformed to meet the needs of our models (logistical regression and multiple linear regression).
  * Dropped values that did not have data for budget.
  * Dropped movies not released in the United States.
  * Converted countries to a count of countries where movie was released.
  * Converted genre to a count of genres it was categorized as.
  * Filtered so that each row had at least seven features that were not null. 
  * Standardized unrated and not rated for genre.
  * converted runtime to an integer.
  * one-hot encoded rating and production companies (must have all of data combined at this point to ensure the same number of features later).

## Multiple Linear Regression Model
Linear regression from sklearn was used. We trained on 2016 and tested on 2017. It had a training score of 0.6195 and a testing score of 0.4431. Such a low test and train score can be attributed a lack of financial data such as production budget, marketing budget etc.

## Logistical Regression Model
Logistic regression from sklearn was used to create the model. Again we trained on 2016 and tested on 2017. It had a training score of 0.9170 and a testing score of 0.9026 for determining if a movie was in the top 20 for box office.
