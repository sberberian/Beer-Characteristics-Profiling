# Beer Characteristics Profiling 

[Click here for the presentation.](https://docs.google.com/presentation/d/1Rn_7RCTm9UO72irvWF4ho0fOMzaHRWQAoMQVw0SUD4k/edit#slide=id.p)

[Click here for the Tableau Public dashboard.](https://public.tableau.com/views/BeerStyleAnalysis/Dashboard2?:language=en-US&:display_count=n&:origin=viz_share_link)

## Overview

The scope of this project is evaluating the flavor profile of successful beers. Since the data analytics program is based in Wisconsin, it seemed like a suitable and fun topic to explore.

The dataset used, Beer Profile and Ratings dataset, is a combination dataset found on Kaggle of two other Kaggle datasets. The first contains flavor profiles of successful beers and the second contains over a million reviews of beers.

The data will be analyzed to understand what factors correlate with a high rating based on data for the beers in the dataset. Our group also intends to investigate how much the appearance of a beer factors into a very positive review. 

## Communication Protocols

Our team will utilize a variety of tools for the duration of the project. Github is the resource for filesharing and collaborating on code. A group calendar has been created with Google Calendar to schedule meetings outside of class. Trello is helping to manage tasks and expectations for the deliverables of each milestone in the project. Slack is being used for messaging between teammates and arranging calls. 

## Dashboard

The project's visualization will be created using Tableau. The interactive elements under consideration are filtering and highlighting data by style and review score between visualizations.

## Machine Learning Model

### Model Choice 

A supervised machine learning model was chosen as the ideal approach for the analysis. Our team will implement a random forest algorith for the following reasons:
* Implementing a random forest algorithm will be useful in reducing likelihood of overfitting;
* it can manage many inputs; and
* it can rank the features easily.

The classification model will effectively return the most important characteristics for predicting a popular beer.

### Data Preprocessing

#### Feature Selection and Engineering 

After reading in the data and examining the features, some features were filtered while unnecessary features were dropped. 

To avoid having the analysis skewed by beers with only a few reviews, the dataframe was refined to include only beers with a number of reviews in the upper quartile.

The target variable, the overall review, was separated into binary values. Our team has determined that a successful beer will have a rating greater than or equal to a 4 star review. If it meets this criterion it is classified as a 1, else it is classified as a 0. 

#### Training and Testing 

The X variable was defined as all of the attributes, such as bitter, sour, hoppy, etc. The target, the Y variable, was set as the overall rating for a beer. A training and testing set was created for both variables. They were scaled and fit to a random forest classifier model to then return training and testing scores. The features were ranked by importance and plotted. Feature selection from the sklearn library was used to choose the important attributes which replaced the original X variable set and fed back into the model to return new scores.  
