---
layout: post
title: Yelp Business Recommendation API
subtitle: Predict and visualize Yelp's data
gh-repo: business-rec/ds
gh-badge: [star, fork, follow]
tags: [business, data science, API, heroku, NLP, scattertext]
comments: true
---
I deployed a Yelp Business Recommendation API (http://br-yelp-predict-rating.herokuapp.com) using machine learning and scattertext to help business owners understand the key elements for different categories.

Using [Yelp's official dataset](https://www.yelp.com/dataset), I trained a model to predict the user's review rating base on reviews on the Yelp dataset in the specific category.

My API takes in a json string with "category" and "review". After sending the input to my API, it will respond with the predicted rating of the review.

When submitting a review, make sure to specify which category the review is for.

Example input:
```python
{"category": "Auto Repair", 
 "review": "Service is okay but the wait time is too long."}
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
