# OLIST Ecommerce - Analysis and Product Recommendation System

![](./assets/olist.png)

This repository is the capstone project for my Juno College Data Analytics Bootcamp. I have used excel, python, and Tableau to investigate OLIST's Eccommerce Data, and build a product recommendation system for their users. The purpose of this project is to test my ivestigative analysis, as well as challenge myself to learn how to use machine learning to build a recommendation system, using a variety of different algorithms and techniques. I still have much to learn and implement, as this is just a prototype version as it stands. 

* Accompanying Dashboard can be found [Here](https://public.tableau.com/app/profile/bailey.wolkoff/viz/OLIST_KPI_Overview/OLISTOverview) where I take an overview look at OLIST's KPI Metrics. 

## The Data
The Data was taken from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) where OLIST had uploaded real ecommerce data. Product, Seller, and Customer ID's were used to protect the privacy of all who would be affected. 

This data came as a set of muiltiple CSV files, each being linked to one another using keys. A Data Schema accompanied the dataset to make this easier and more straightforward on the user:

![](./assets/schema.png)

The Files used are:
1. customers_dataset.csv
1. geolocation_dataset.csv
1. order_item_dataset.csv
1. order_payments_dataset.csv
1. order_reviews.csv
1. orders_dataset.csv
1. products_dataset.csv
1. sellers_dataset.csv
1. product_category_name_translation.csv

## Ethical Concerns

The Data used unidentifiable keys to protect customer and seller privacy. It should however be noted that a recommendation system can have concerns, as it may suggest a product for a user that is deemed inappropriate. This is currently unavoidable as I do not have information on the user, or the actual product name. I am also missing a lot of information on customers, and only have the rough location (City) from which they placed their order. 

## References
* Big thank you to [Yohan Jeong](https://towardsdatascience.com/item-based-collaborative-filtering-in-python-91f747200fab) who's article on item based collabrotive filtering I followed very closely for my preliminary model.
* [Krish Naik](https://www.youtube.com/watch?v=R64Lh1Qwl_0) who's youtube videos helped understand collaborative filtering. 
* [Anna Barentz](https://public.tableau.com/app/profile/annabarentz/viz/E-CommerceDashboardOlist/Dashboard3) who's Dashboard inspired me. 






Notes: 
* order_item_id is like that particular item number if customer ordered more than 1 one of the same product in that order
    * to find how many of a particular item was ordered: groupby('order_id')['order_item_id'].max()
    
* want to look at most purchased category by month
    * need to join with orders to find purchase month
