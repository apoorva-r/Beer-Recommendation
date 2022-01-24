# Beer Recommendation

Follwed tutorials from [here](https://github.com/mxie87/Beer_Recommender_CF)  and [here](https://github.com/ameyakarnad/BeerPersonalization)

Created a recommendation system that will take a beer name as an input and return the top N recommendations based on item similiarity. Collaborative Filtering and content-based filtering approaches were researched and several algorithms like KNN, SVD, Matrix-factorization were also implemented. Data was collected from BeerAdvocate dataset(https://www.beeradvocate.com/) and stored on the local machine.

The Data:
56 subcategories of beer
4964 unique beers
~88K unique users
~1.4M user-review pairings

Main Tools:
Surprise Library - http://surpriselib.com/
scikit-learn: https://scikit-learn.org/stable/
