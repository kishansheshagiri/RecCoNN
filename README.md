# RecCoNN

This is our implementation for the Information Retrievel Course Project. We have extended DeepCoNN architecture proposed by Lei Zheng et. al. in Jan 2017 which is the state-of-the-art method that utilizes deep learning technology to jointly model user and item from textual reviews.

Two models:

1、RecCoNN: Included additional User Profile specific features.

2、DeepCoNN+attributes: Appended User reviews with additional attributes informations relavent to that review.

Network Analysis:

1. Created Heterogeneous Information Network (HIN) and analysed the percentage of users depending on their friends recommendations. Also in future, we would like to think about additional algorithms to add Edge weights based on different relations among nodes. We hope including these edge weights in the Loss function may improve the results.

## Environments

- python 2.7
- Tensorflow (version: 0.12.1)
- numpy
- pandas


## Dataset

Yelp Challenge 2017(https://www.yelp.com/dataset_challenge).

## Example to run the codes		

Data preprocessing:

```
python cleanup.py
python cleanup_state.py
python load_yelp.py	         [This is for DeepCoNN and RecCoNN (wuf)]
python data_pro.py           [This is for DeepCoNN and RecCoNN (wuf)]
python load_yelp_wattr.py    [This is for DeepCoNN with attribute (wattr)]
python data_pro_wattr.py     [This is for DeepCoNN with attribute (wattr)]
```

Train and evaluate the model:

```
python train_wuf.py          [This is for DecCoNN with attributes appended to the users reviews]
python train_waatr.py        [This is for RecCoNN]
```



Last Update Date: Apr 23, 2018
