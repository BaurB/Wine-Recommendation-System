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
Vivino.com is an online marketplace that has more than 10 million wines and 35 million registered users. Data Scraping was done using the REST API. I have logged my network traffic using Google Chrome's dev tools and obtained a JSON response with information for different wines. Then, I filtered and selected the required wine information that will be useful for the project. The selected variables are as follows: winery, wine_year, wine_rating, wine_price, wine_region, wine_country, grape_information, wine_acidity, wine_intensity, wine_sweetness, wine_tannin wine_description. Collected features used in the EDA and Recommendation System buildup. It should be noted that website response does not contain all features and for some wines, all variables will be given, while for others it will be empty. Overall, I was able to generate 21,981 unique wines with different categories. Performed EDA gave the following insights:

  1. Wine data by category:

  | Wine Category | Number of Wines |
  | ------------- | ------------- |
  | Red           | 10287         |
  | White         | 6074          |
  | Sparkling     | 2230          |
  | Rose          | 1534          |
  | Dessert       | 1020          |
  | Fortified     | 811           |

  2. The majority of the database (over 50%) reflects wine bottle pricing under $ 50 with most of the wines produced in the last few years
  
  3. Most of the Wines have a user rating between 3.7 and 4.3 out of 5.0
  
  4. Order of the top five wine styles Cabernet Sauvignon, Chardonnay, Shiraz/Syrah,  Pinot Noir and Sauvignon Blanc. The order of the top five wine-producing countries is as follows: France, United States, Italy, Spain and Portugal.
  
  5. A moderate positive correlation between wine rating and the price was observed when the wine rating was 4.0 and higher

Other interesting insights can be found in the Jupyter notebook. 

During the construction of the User Rating dataset, I realized that most of the wines do not have a high amount of reviews, some of them having a few reviews each. Therefore, I simulated data based on the average consumer ratings scraped for every observation. This allows building a rating based recommendation system by measuring cosine similarity.

Finally, the Recommendation system based on the Wine Description was build using sklearn's TFIDF Vectorize feature to convert text data to numeric variables that we can use to find similarities between the input wine and other data in the gathered dataset.

## Conclusions and Future Work
Developed User-Ratings based Recommender shows promise and recommends wines that have a similarity of 0.5 and higher. Should be noted that it only focuses on wine ratings:

![image](https://user-images.githubusercontent.com/80535531/113145835-608bb000-9248-11eb-89e5-468a4e18d33a.png)

For Wine Description Recommender testing, 5 wines were searched with one of them being a Sparkling Wine and the rest are Red Wines. Three wines were recommended for each inputted Wine and all of the recommendations were in the appropriate wine price and winery location.

![image](https://user-images.githubusercontent.com/80535531/113157266-2f18e180-9254-11eb-89f2-e5236856ed41.png)
One big flaw of the description recommender system lies in the quality of gathered data since the majority of the wines that have the same winery location/grape information have the **same description** as well. This can be resolved by gathering/scraping high-quality data from the web.

For the depth and complexity we seek for this recommender, there is a future work required:
* **Obtain a more robust wine dataset:** Spend more time on scraping high - quality data from other wine marketplace or purchase a much larger wine list dataset, with more depth of profile characteristics. It would improve the recommender results
* **Consider using Collaborative Filtering Recommender System instead of Content based one:** k nearest neighbors will help to identify clusters of similar users based on common wine ratings, and make a suitable recommendations
* **Develop a nice Front-End interface:** User/customer can type a wine/list of wines that he liked and get a suitable recommendations.
   
In conclusion, this project has only scratched the surface and there is still a lot of potential in producing a recommder system that simplifies the development of a restaraunt's wine list. I will continue developing the project further and present a better working recommender system




