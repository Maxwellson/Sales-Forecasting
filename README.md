# Time series regression project: Sales Prediction
Introduction

Corporation Favorita is an organization based in Ecuador which sets up department stores and supermarkets. They are involved in the retail sale of a wide range of goods, including groceries, cars, and real estate. For this project, I examined sales data from various stores across the country to gain insights into the products and sales made on a daily basis over the course of five years. The goal is to forecast future sales using current sales data.

I used the CRISP-DM framework as the methodology for this assignment.

Datasets

train.csv

The training data, comprising time series of features (01–01–2013 to 15–08–2017), store_nbr, family, and on promotion as well as the target sales.
store_nbr identifies the store at which the products are sold.
family identifies the type of product sold.
sales give the total sales for a product family at a particular store at a given date. Fractional values are possible since products can be sold in fractional units (1.5 kg of cheese, for instance, as opposed to 1 bag of chips).
On promotion gives the total number of items in a product family that were being promoted at a store at a given date.
test.csv

· The test data has the same features as the training data. Prediction was based on the target sales for the dates in this file.

· The dates in the test data are for the 15 days after the last date in the training data (15–08–2017).

transaction.csv

· Contains date, store_nbr and transaction made on that specific date.

stores.csv

Store metadata, including city, state, type, and cluster.
cluster is a grouping of similar stores.
oil.csv

Daily oil price which includes values during both the train and test data timeframes. (Ecuador is an oil-dependent country and its economic health is highly vulnerable to shocks in oil prices.)
holidays_events.csv

· Holidays and Events, with metadata

Hypothesis

Null hypothesis: Product sales are directly correlated with special events.

Alternate hypothesis: Product sales are independent of events.

Questions

Which dates have the lowest and highest sales for each year and which year recorded many sales? Which time of year are most purchases made

2. A magnitude 7.8 earthquake struck Ecuador on April 16, 2016. Did the earthquake impact sales?

3. Are certain groups of stores selling more products? (Cluster, city, state, type) and which family of products are the most purchased?

4. Are sales affected by promotions, oil prices and holidays?

Data understanding

After the preliminary data exploration, I noticed that the train and test datasets were highly important. The additional datasets were the oil, transactions, stores and holiday datasets. The first task was to clean the datasets and get rid of duplicates and null values. After going through the above process, I realized that the primary datasets had no duplicates and null values. However, based on the questions and modelling aspect, left join was performed on the supplementary datasets. Missing values in the additional datasets were backfilled and for categorical missing values like for the holiday data, it was filled with no holiday.
