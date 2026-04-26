# B1 -Problem Formulation # 
(a) ML Problem

The target variable is number of units sold

The candidate input features are type of promotion, store size, customer dempgraphics(age, gender, etc), location of store, competition.

Type of ML problem: This is a regression problem because we are predicting continuous values which is sales. We want to predict or estimate how many number of items will be sold under each promotion.

(b) Why items sold instead of revenue

The total sales revenue is based of variety of factors such as different offers, seasons,price, etc. which may not exactly tells us about the perfomance of the company. 
for ex, seasonal sales could increase the revenue in one month while decline the sales in another which could be misleading. 
Items sold (sales volume) is a more reliable target variable as it will consider the actual demand and would help us to understand how customers react to the promotional campaings.
This would be a better target variable as it matches the business objective of maximising the number of items sold.

(c) Alternative to one global model

The suggestion of running one single global model across all 50 stores may not be effective. Because different locations wil have different customer base and dempgraphics that will affect the sales. So it will be difficult to compare the results
Therefore instead of one model for all stores, we can use separate models for different store types. Such as Category-Specific Offer or Loyalty Points Bonus for Urban areas, Free Gift with Purchase for semi-urban and BOGO or flat dicounts for Rural areas. 
Different locations perform differently therefore separate models will give more accurate results. 


# B2-Data and EDA Strategy #

(a) Joining the table and Datasets

I have four separate tables: transactions, store attributes, promotion details, and a calendar (with weekend and festival flags).
Start with transactions table as a base, join store attirbutes using store_id, and we join promotion details table------------------ and join calendar on the transaction date

The grain of the final modelling dataset would be one row= one store on one day. This will help in analysing and predciting sales voulme at each date. 

Aggregation before modelling: 1. Total item sold per store each day. 2. Promotions applicable for a day in store 3. Festival flag/weekend flag.
These aggregations will help us estimate the sales impact of each promotion on a certain day at each store. 

(b) EDA 

EDA helps us to understand the dataset in order to predict values or detect anomalies(faults) for modelling. Before building a model, I would understand all the coloums and the relationship between them such as the store locations, dates ,type of promotions,etc. Check the type of data(text,integer ,date) 
Find any anomlaies and dentify missing values or inconsistencies. I would also take help of visualisation tools such as charts,bars, heatmaps,etc to understand the data from different angles. 

Types of analyses or charts: 

1.Bar chart  (promotion vs sales) 
To analyse how different types of promotionsacross different store locations, it would help me choose those promotions which works best for a particular location. 

2. Line chart (for seasonal or monthly trend)
This will help me understand when the sales are at peak for a particular item on a particular store on a particular day/month.

3. 
