# Introduction

Imagine that you are a data scientist at a news publisher wanting to personalize which article a user sees. You can choose to let the user see the latest story in one of these 8 categories:

1. News
2. Sport
3. Business
4. Tech
6. Health & Fitness
7. Money
8. Opinion

## The problem

To create a recommender system you have the following dataset at your disposal.

```
> import pandas as pd
> df = pd.read_pickle("df.pickle")
> df.head
```

|    |   id |   geography |   current_topic |   visit_count_30_days |   most_favorite_topic |   least_favorite_topic |   topic_shown |
|---:|-----:|------------:|----------------:|----------------------:|----------------------:|-----------------------:|--------------:|
|  0 |    0 |           1 |               0 |                     6 |                     0 |                      3 |             0 |
|  1 |    1 |           0 |               0 |                    64 |                     0 |                      2 |             0 |
|  2 |    2 |           1 |               0 |                    22 |                     4 |                      3 |             6 |
|  3 |    3 |           2 |               0 |                    52 |                     4 |                      3 |             0 |
|  4 |    4 |           0 |               0 |                    35 |                     0 |                      2 |             0 |

The case of [Tomi Lahren](https://www.csmonitor.com/USA/2016/1203/The-Daily-Show-attempts-to-pop-the-news-bubble-with-a-conservative-guest) is an example of what can occur if optimise news curatation by geography. You want to make sure that you are not creating similar *filter bubbles* with you recommender system.

Filter bubbles in news curating is a major problem. The [U.N. investigators](https://www.reuters.com/article/us-myanmar-rohingya-facebook/u-n-investigators-cite-facebook-role-in-myanmar-crisis-idUSKCN1GO2PN) cite Facebook's recommender system role in Myanmar crisis and [The "Yellow Vest" Riots In France](https://www.buzzfeednews.com/article/ryanhatesthis/france-paris-yellow-jackets-facebook) is believed to be a consequence of changes to Facebook algorithms.

## The solution

In this seminar we will show you how you can meassure the geographic bias in your data as well as in a news recommender system built with Tensorflow using the IBM AI Fairness 360 Framework. Follow along in the notebook.