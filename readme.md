# Personalisation Project 

NOTE: The personalisation final report mostly contains the results that we obtained during the course of the project. The individual models are explained in seperate files, for which links have been provided in the final report. 

## Contents
- Personalisation_final_report.ipynb : The final Report
- Models/ : Contains the 4 files with KNN model, Content based model (CBM) , Matrix factorisation(SVD and NMF), Popular items for cold start
- Others/ : Other files


## Approach
Our recommendations are based off a number of different approaches, each of them targeting to one of more business challenges:
- Collaborative filtering/model based methods (targeting challenge #1)
- Popular items (#3, #4)
- Item based features (#2, #3)
- User Preferences (#4)

## Data Source
For this exercise, we used data from the popular beer review website BeerAdvocate.com (available at https://snap.stanford.edu/data/web-BeerAdvocate.html).

## Description
During the first phase, we focused on implementing two brute-force collabrative filterings to predict the user ratings for certain beers: neighborhood-based (including user-based and item-based) and model-based (specifically matrix factorization). We tested and compared the result of collaborative filtering approaches (both item and user based) and matrix factorization. Both models were developed using only the overall beer ratings (from 1 to 5), but we plan to expand the number of features in future iterations.

For the first phase, we focused our initial analysis on a subset of top 1,000 users and top 100 beers by number of reviews. We initially implemented item-based collaborative filtering using pandas dataframes, but due to performance issues we ultimately opted for a different implementation of collaborative filtering which leverages numpy arrays. Our initial findings shows that the user based collaborative filtering approach achieves the lowest RMSE and MAE for unobserved beer ratings (0.529 and 0.4 respectively), compared to SVD and NMF which achieved RMSE of 0.54 and 0.55 respectively. We suspects these results are in part due to the way we constructed our initial review subset, so we plan to test the performance of these approaches for larger and sparser datasets in the near future.

The "Final_Report" folder includes two jupyter notebooks which show how we trained and tested our final collaborative filtering and matrix factorization approaches respectively. The "Dataset" folder contains the subset of the dataset that we used for this initial phase. The "Others" folder includes obsolete files, including our initial item-based collaborative filtering implementation.
