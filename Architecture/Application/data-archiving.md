# Data Archiving

## Description

Every solution needs to hold historical data for several reasons, from legal to technical.
In this scenario, the team considered it prudent to store all the transactions recorded by users, the points given/earned, the goods acquired, the donations made, etc.

This can help anyone to build balance through time, and on the other side for Merchants to track their catalogs, how the stock changed, and which products could be better to offer perhaps.

So it’s important to build an analytics platform backed with accurate and durable information.
   
Therefore, to go with KISS principle, considering the cost is the key driver, the historical datastore will be held in S3 buckets, with proper aging/archiving tiering (glacier, deep glacier). The archiving strategy can be defined together with the business, same as data retention period. 
