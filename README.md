# Polimi Recommender System challenge A.Y. 2022/23

This repo contains the code and the data used in the [Recommender Systems 2022 Challenge](https://www.kaggle.com/competitions/recommender-system-2022-challenge-polimi/overview) @ Politecnico di Milano.

## Description

The application domain is TV shows recommendation. The datasets we provide contains both interactions of users with TV shows, as well as features related to the TV shows. The main **goal** of the competition is to discover which items (TV shows) a user will interact with.

The **datasets** includes around 1.8M interactions, 41k users, 27k items (TV shows) and two features: the TV shows length (number of episodes or movies) and 4 categories. For some user interactions the data also includes the impressions, representing which items were available on the screen when the user clicked on that TV shows.

## Evaluation

The evaluation metric for this competition is **MAP@10**.
The average precision at 10, for a user is defined as:

#### $$\\textrm{AP}@10 = \sum\_{k=1}^{10} \frac{P(k) \cdot \textrm{rel}(k)}{\textrm{min}(m, 10)}$$

where *P(k)* is the precision at cut-off *k*, rel(*i*) is 1 if item in position *k* is relevant, 0 otherwise, and *m* is the number of relevant items in the test set. The mean average precision for N users at position 10 is the average of the average precision of each user, i.e.,

#### $$\textrm{MAP}@10 = \frac{\sum_{u=1}^{} {\textrm{AP}@10\_{u}}}{N}$$

## Results

1. **Public leaderboard:** 4th place
2. **Private leaderboard:** 4th place

We manage to obtain a **MAP@10: 0.06128**

## Best model

The final model is a hybrid recommender composed of **6 different algorithms**:
- Slim ElasticNet (Stacked URM)
- Rp3Beta
- ItemKNNCF
- EASE-R (Stacked URM)
- SlimBPR
- ImplicitALS

## About us

[Davide Zanutto](https://github.com/DavideZanutto) and [Alessandro Rossi](https://github.com/AlexRouge)
