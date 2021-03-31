# Wine-Recommendation-System
The global Wine market is projected to increase by more than 30 per cent in the 7 years with a high influx of new customers. In current economical conditions, it is crucial to productively develop a wine list that will fit customers needs. Greatly developed wine lists can effectively complement the food which in turn brings more profit. Therefore, businesses (restaurants, wine shops) will need to find a balance between an engaging wine list and managing inventory to avoid stock-outs.  

Real-time consumer-driven information can be provided to restaurants and other beverage businesses to know more about local market wine preferences and reduce the time and resources to create their wine list, while increasing sales of proven, popular wine brands and styles.

## Objectives:
This project is focused on building a recommendation system and analyse the current state of wine market. It is done through the following steps:

* Construct a databse based on the scraped from the popular consumer wine website vivino.com
* Perform Exploratory Data Analysis on 21,981 unique wines and identify biggest wine producers, wineries, average ratings and other features
* Build a User Rating Dataset for Recommendation System
* Build User Rating based Recommendation System
* Build Wine Description based Recommendation System

## Executive Summary:
Vivino.com is an online marketplace has more than 10 million wines and 35 millions registered users. Data Scraping was performed using the REST API. I have logged my network traffic using Google Chrome's dev tools and obtained a JSON response with information for different wines. Then, I filtered and selected the required wine information that will be useful for the project. The selected variables are as follows: winery, wine_year, wine_rating, wine_price, wine_region, wine_country, grape_information, wine_acidity, wine_intensity, wine_sweetness, wine_tannin wine_description. Those features will be used in the EDA and during building the Recommendation System. It should be noted that website response does not contain all features and for some wines, all variables will be given, while for others it will be empty. Overall, I was able to generate 21,981 unique wines with different categories




![image](https://user-images.githubusercontent.com/80535531/113129078-ed783e80-9233-11eb-8d14-ea3c8e98f8e7.png)

