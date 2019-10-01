---
layout: post
title: Insuline Diabetes Manager App
subtitle: Track and predict blood glucose measurement
gh-repo: Build-Week-Diabetes-Manager/DS-Heroku
gh-badge: [star, fork, follow]
tags: [health, data science, app, predictive modeling, heroku]
comments: true
---
![homepage](https://github.com/gyhou/gyhou.github.io/blob/master/img/diabetes%20manager%20homepage.png?raw=true)

My team deployed an app [Insuline Diabetes Manager](https://diabetesmanager.netlify.com/) to help diabetic patients track and predict blood glucose levels!

Using the [Michael Kahn, MD, PhD](https://archive.ics.uci.edu/ml/datasets/diabetes) dataset, our data science team and I trained a model to predict user's future blood glucose level base on insulin intake, previous measurements and the time it was measured.

[Blood glucose measurement prediction API](http://diabetes-manager-app.herokuapp.com)

Example input:
```python
val = [{"id": 1,
        "timestamp": "2000-10-10 7:10",
        "code": 33,
        "value": 10.0,
        "user_id": 1},
       {"id": 2,
        "timestamp": "2000-10-10 9:10",
        "code": 59,
        "value": 100.0,
        "user_id": 1},
       {"id": 3,
        "timestamp": "2000-10-10 11:10",
        "code": 60,
        "value": 180.0,
        "user_id": 1},
       {"id": 4,
        "timestamp": "2000-10-10 19:10",
        "code": 63,
        "value": 250.0,
        "user_id": 1},
       {"id": 5,
        "timestamp": "2000-10-10 22:10",
        "code": 57,
        "value": 300.0,
        "user_id": 1},
       {"id": 6,
        "timestamp": "2000-10-11 9:10",
        "code": 33,
        "value": 5.0,
        "user_id": 1},
       {"id": 7,
        "timestamp": "2000-10-11 10:10",
        "code": 59,
        "value": 150.0,
        "user_id": 1},
       {"id": 8,
        "timestamp": "2000-10-11 13:10",
        "code": 60,
        "value": 200.0,
        "user_id": 1},
       {"id": 9,
        "timestamp": "2000-10-11 18:10",
        "code": 63,
        "value": 100.0,
        "user_id": 1},
       {"id": 10,
        "timestamp": "2000-10-11 00:10",
        "code": 57,
        "value": 180.0,
        "user_id": 1},
       {"id": 11,
        "timestamp": "2000-10-12 8:10",
        "code": 33,
        "value": 7.0,
        "user_id": 1},
       {"id": 12,
        "timestamp": "2000-10-12 8:10",
        "code": 59,
        "value": 90.0,
        "user_id": 1},
       {"id": 13,
        "timestamp": "2000-10-12 12:10",
        "code": 60,
        "value": 130.0,
        "user_id": 1},
       {"id": 14,
        "timestamp": "2000-10-12 20:10",
        "code": 63,
        "value": 150.0,
        "user_id": 1},
       {"id": 15,
        "timestamp": "2000-10-12 23:10",
        "code": 57,
        "value": 200.0,
        "user_id": 1}]
```
        
        
Example Output:
Response was
```json
{'Pre-breakfast 07:23AM measurement': 185.87, 'Post-breakfast 09:56AM measurement': 168.67, 
'Pre-lunch 12:09PM measurement': 119.76, 'Post-lunch 14:20PM measurement': 201.92, 
'Pre-supper 17:52PM measurement': 122.47, 'Post-supper 19:11PM measurement': 138.75}
```
