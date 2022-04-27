# OLIST Ecommerce - Analysis and Product Recommendation System

This 


## References
* Big thank you to [Yohan Jeong](https://towardsdatascience.com/item-based-collaborative-filtering-in-python-91f747200fab) who's article on item based collabrotive filtering I followed very closely for my preliminary model.
* (Krish Naik)[https://www.youtube.com/watch?v=R64Lh1Qwl_0] who's youtube videos helped understand collaborative filtering. 
* [Anna Barentz](https://public.tableau.com/app/profile/annabarentz/viz/E-CommerceDashboardOlist/Dashboard3) who's Dashboard inspired me. 


Notes: 
* order_item_id is like that particular item number if customer ordered more than 1 one of the same product in that order
    * to find how many of a particular item was ordered: groupby('order_id')['order_item_id'].max()
    
* want to look at most purchased category by month
    * need to join with orders to find purchase month
