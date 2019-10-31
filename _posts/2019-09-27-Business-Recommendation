---
layout: post
title: Yelp Business Recommendation API
subtitle: Track and predict blood glucose measurement
gh-repo: business-rec/ds
gh-badge: [star, fork, follow]
tags: [business, data science, API, heroku, NLP, scattertext]
comments: true
---
I deployed a Yelp Business Recommendation API (http://br-yelp-predict-rating.herokuapp.com) using machine learning and scattertext to help business owners understand the key elements for different categories.

Using [Yelp's official dataset](https://www.yelp.com/dataset), I trained a model to predict user's future blood glucose level base on insulin intake, previous blood glucose measurements and the time it was measured.

My API takes in a json string inside a list of measurements, preferably 3+ days worth of measurements around breakfast, lunch and dinner. After sending the input to our API, it will respond with measurements predicting the next day blood glucose level before and after each meal.

Below are the list of categories used in the Yelp dataset:
⋅⋅* Active Life
⋅⋅* Auto Repair
⋅⋅* Automotive
⋅⋅* Beauty Spas
⋅⋅* Contractors
⋅⋅* Doctors
⋅⋅* Event Planning Services
⋅⋅* Fashion
⋅⋅* Fast Food
⋅⋅* Hair Salons
⋅⋅* Health Medical
⋅⋅* Home Garden
⋅⋅* Home Services
⋅⋅* Local Services
⋅⋅* Professional Services
⋅⋅* Real Estate
⋅⋅* Shopping 

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
