# stock price prediction based on historical data and current affairs.

## Problem statement:
    Stock prediction is usually done using historical data but not using current affairs,
    since stocks market is exreamly volatile and are affected by external factor and situations.

## Solution:
    Because of these external factors the models dont take them into consideration this issue can be solved by calculating a news affect based on how revalent the news is to the conpany and how it impacts to the company(can use positive or negative or neutral) combined with the past data this should give much better results compared to the conventional methods.


## Requirments:
  ### 1. functional requirments:
  - data Scraping and storage to processing the effect of the new.
  - model performance must be better than the conventional approaches
  - notification and regular app
  - respective backend.
### 2. Non functional requirments 
-   database duralibility 
-   kafka consistency
-   redis usage to prevent redundant data processing.
-   scalibilaty 
-   extendability
-   maintainable
  
  ## System OverView 
  ### 1. Data Ingession
  - Scraping 
    * data ingession is our data scraping script which aggrigates all news that can affect the stock market and dump it in a table for futher processing.
- HTTP request for the usual api calls 
### 2. Real time Processing
- Real time scraping 
  * This need to be done so that the model can predict the news affect in real time and helping the user using it.
- Real time prediction
  * Real time prediction to be made by the model to keep the data upto date and revalent
- Storage  
    * Mysql for Relational data.
    * ClickHouse for time series data
### 3. Comunication type
- Stateless Apis
### 4. Acrhitecture type and Components
    Employing microService architecture for faster prediction and load balancing and scalling.
- Application Server 

        Java Spring boot application
- Application client

        android app which can recive notifications.
- Model Server

        Python Server Serving and Scraping data  
  
### 5. Cashing and Event handling
- Kafka for handling events.
- Kafka Stream (may need)
- Redis for Cashing

### 6. Models 
- News Catagorization model.
- News affect prediction model.
- Stock Price Prediction model.