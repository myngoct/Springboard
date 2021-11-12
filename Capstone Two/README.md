# Predicting Stroke

Working with a stroke prediction dataset from [Kaggle](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset), I set to implement a machine learning model that can predict with over 95% accuracy whether a patient is likely to have a stroke based on various attributes such as:
- Gender
- Age
- Presence of disease
- BMI (body mass index)
- Glucose level
- Smoking status

## Project Outline

### 1. Data Wrangling

In this [notebook](http://localhost:8890/notebooks/Desktop/Data%20Science/Capstone%20Two/01%20Stroke%20Data%20Wrangling.ipynb), I clean up the raw data by transposing the data so that the rows and columns respectively consisted of variables and observations . I also dropped all the rows with missing BMI data. As the raw dataset was fairly clean, no further data wrangling was required. 

### 2. EDA

In this [notebook](https://github.com/myngoct/Springboard/blob/main/Capstone%20Two/02%20Stroke%20Data%20EDA.ipynb), I identified the stroke column as my target variable and separated the other variables by numerical and categorical features to create data visualizations. I also plotted a heat map to see if there were any high correlations between the atrributes and getting a stroke. 

### 3. Data Pre-Processing, Training, and Modeling

In this last [notebook](https://github.com/myngoct/Springboard/blob/main/Capstone%20Two/03%20Stroke%20Data%20Pre-processing%2C%20Training%2C%20and%20Modeling.ipynb), I calculated the accuracy of various algorithms and used ROC curve analysis and cross validation in order to determine the best model. I also implemented a few classifier models to determine the variables that held the highest feature importance.

### 4. Conclusion

From this stroke dataset, I found the logistic regression model to have the highest accuracy in predicting stroke. The variables that held the most importance were: average glucose level, age, and BMI. Going forward, there can be some adjustments made to improve this project. Firstly, the size of the data was on the smaller scale, with less than 5,000 entries, so if more data could be collected, it would greatly improve the validity of the algorithm. Secondly, the data was not well-balanced, as most of the patients in the data did not have a stroke. It would have been better we could have recorded more data for patients that did have a stroke to imporove the model. Lastly, it would also be helpful to have included the demographics of the patients as this is an important attribute to analyze and apply to the population.   
