# Glassdoor ML Challenge
The goal is to build a classification to accurately predict if a user applies to a job position or not. 

# Dataset
    1) title proximity tf idf: Measures the closeness of query and job title.
    2) description proximity tf idf: Measures the closeness of query and job description.
    3) main query tf idf: A score related to user query closeness to job title and job description.
    4) query jl score: Measures the popularity of query and job listing pair.
    5) query title score: Measures the popularity of query and job title pair.
    6) city match: Indicates if the job listing matches to user (or, user-specified) location.
    7) job age days: Indicates the age of job listing posted.
    8) apply: Indicates if the user has applied for this job listing.
    9) search date pacif: Date of the activity.
    10) u id: ID of user (for privacy reasons ID is anonymized).
    11) mgoc id: Class ID of the job title clicked.

# Code and Analysis

Dataset was divided into training and testing data based on the search_date_pacific feature.

All records on 01/27/2018 were used as test data and the remaining as training data.

Data analysis was followed by correlation estimation and different machine learning models were applied to the dataset.

The dataset represents imbalanced data where the records of label apply = 1 were 24% only. 

This leads to high accuracy but low f1 score.

Model building and testing was first done on the first seven columns, and then the last two columns were added to aboserve any changes to predictions.

Further, imblearn package was explored to deal with imbalanced dataset [ ... in progress ]

# Credits
The dataset is provided by Glassdoor for it's ML Intern interview process. I own no rights to this data.

I merely built a model to analyze this dataset and predict apply rates.
