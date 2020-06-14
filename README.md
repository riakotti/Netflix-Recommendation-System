# Netflix-Recommendation-System
 
I played with building a reccomendation system for movies.

I started with a basic popularity model (does not take into account user's and item's similarities). 

* Method 1: Recommend movies based on the *overall* most popular choices among *all* the users

* Output 1: All the users receive the same recommendations 

Then I focused on a recommendation engine with collaborative filtering.
   
*  Method 2: User-based collaborative filtering  (UBCF) - Recommend movies based on the other 'similar' users (similarity measued using nearest neighbor approach).
*  Output 2: Users that belong to same clusters have the same recommendations (the recommendations are different to the users that belong in a different cluster)

* Method 3: Item-based collaborative filtering (IBCF) - Recommend movies based *on past personal preferences* (similar items)

* Output 3: Different users will have a different set of recommendations according to individual's history - personalized recommendations

In the current version I do not yet apply a hybrid approach. This is a method that combines collaborative filtering and content-based approaches and it is commonly used in many large-scale recommender systems. The easiest way to apply the hybrid approach is to *independently* train one collaborative filtering model and one content based model and combine their suggestions to create the final reccomendation. A more advanced way to apply the hybrid approach is to *directly* build a single model (often a neural network) that uses as input prior information about the user, item, and their interactions.

Click [here](https://www.kaggle.com/netflix-inc/netflix-prize-data/download) to download the data.

## Scripts

  * data_manipulation.ipynb - data manipulation for movie data (save the output as 'df.csv' file)
  * exploratory_analysis.ipynb - exploratory data analysis (EDA)
  * recommendation_systems.ipynb - effective movie recommendation system, which also solves the cold-start problem
  
