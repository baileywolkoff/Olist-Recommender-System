Notes: 
* order_item_id is like that particular item number if customer ordered more than 1 one of the same product in that order
    * to find how many of a particular item was ordered: groupby('order_id')['order_item_id'].max()
    
* want to look at most purchased category by month
    * need to join with orders to find purchase month
