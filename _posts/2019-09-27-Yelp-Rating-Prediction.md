---
layout: post
title: Yelp Rating Prediction API
subtitle: Explore and predict Yelp's data
gh-repo: gyhou/yelp_dataset
gh-badge: [star, fork, follow]
tags: [business, data science, API, heroku, NLP, predictive modeling]
comments: true
---
I deployed a Yelp Rating Prediction API (http://br-yelp-predict-rating.herokuapp.com) using [Yelp's open dataset](https://www.yelp.com/dataset) and machine learning to train a model to predict reviews base on different categories.

I wrote an article [Convert Yelp Dataset to CSV](https://towardsdatascience.com/converting-yelp-dataset-to-csv-using-pandas-2a4c8f03bd88) to demonstrate a step-by-step of how to load the gigantic file of the Yelp dataset, notably the 5.2 gigabytes worth of review.json file to a more manageable CSV file. With over 6 million reviews in the review.json file, it could be troublesome to load inside a Jupyter Notebook. After successfully converting the dataset, check out my next post for [explorative analysis](https://towardsdatascience.com/analyzing-yelp-dataset-with-scattertext-spacy-82ea8bb7a60e) of the dataset!

My API takes in a json string with "category" and "review". After sending the input to my API, it will respond with the predicted rating of the review.

When submitting a review, make sure to specify which category the review is for.

Example input:
```python
{"category": "Auto Repair", 
 "review": "Service is the worst and the wait time is too long."}
```
The API will return a rating base on the category and review.
Example Output:
```python
{'Category': 'Auto_Repair',
 'Review': 'Service is the worst and the wait time is too long.',
 'Predict rating': 1}
```

Below is the list of categories used in the Yelp dataset:
* Active Life
* Auto Repair
* Automotive
* Beauty Spas
* Contractors
* Doctors
* Event Planning Services
* Fashion
* Fast Food
* Hair Salons
* Health Medical
* Home Garden
* Home Services
* Local Services
* Professional Services
* Real Estate
* Shopping 
