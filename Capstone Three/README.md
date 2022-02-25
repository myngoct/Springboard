# Time Series Forecasting

Working with information provided by [Kaggle](https://www.kaggle.com/c/store-sales-time-series-forecasting) on Corporación Favorita, a large Ecuadorian-based grocery retailer, I set to predict store sales using time series forecasting. 

---

## Project Outline

 ### 1. Data Wrangling & EDA

In this [notebook](https://github.com/myngoct/Springboard/blob/main/Capstone%20Three/01%20Store%20Sales%20Time%20Series%20Forecasting%20Data%20Wrangling%20and%20EDA.ipynb), I clean the raw data and analyzed it. The training data includes dates from 2013-01-01 to 2017-08-15 and the test set comprises dates from 2017-08-16 to 2017-08-31.

The training data contained features such as: <b>store_nbr</b>, <b>family</b>, <b>onpromotion</b>, and <b>sales</b>:
- <b>store_nbr</b> refers to the store at which the products are sold
- <b>family</b> refers to the type of product sold
- <b>onpromotion</b> gives the total number of items in a product family that were being promoted at a store on a given date
- <b>sales</b>, the target feature, gives the total sales for a product family at a particular store at a given date. Fractional values are possible since products can be sold in fractional units (1.5 kg of cheese, for instance, as opposed to 1 bag of chips).

I made visuals to track the shopping trends of the sales and transactions to help the stores identify popular product families, which months are projected to be busy, and how putting a product on promotion affects the sales.

### 2. Pre-processing and Modeling

In this [notebook](https://github.com/myngoct/Springboard/blob/main/Capstone%20Three/02%20Store%20Sales%20Time%20Series%20Forecasting%20Pre-processing%20and%20Modeling.ipynb), I created a time series forecast using the DirRec strategy which trains a model for each step and uses forecasts from previous steps as new lag features. Step by step, each model gets an additional lag input. To prepare the dataset for modeling, a 16-step forecast with a 1-step lead time is needed using, lags starting with lag 1 and making the entire 16-step forecast with features from 2017-08-15. Root Mean Squared Logarithmic Error is used as the metric for evaluation. 


### 3. Conclusion

Analyzing the training data revealed:
- There is a sharp increase in number of transactions towards the end of the year
- The busiest day of the week is Saturday
- Grocery I, Beverages,  Produce, Cleaning, and Diary are the top 5 selling product families 
- Products on promotion are correlated with a higher number of sales

Employing the DirRec Strategy, a 16-step forecast with a 1-step lead time is used to build the  time series. The predicted values were compared to the actual test values using Root Mean Squared Logarithmic Error (RMSLE) as the metric, and verified the actual values were very close to the predicted values. This information would be very useful to help the stores reduce food waste by knowing when to increase or decrease inventory according to the trends of customer demands. 

