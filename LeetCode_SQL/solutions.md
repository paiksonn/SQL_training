- #1757 Recyclable and Low Fat Products [link](https://leetcode.com/problems/recyclable-and-low-fat-products/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select product_id
from Products
where (Products.low_fats = 'Y') and (Products.recyclable = 'Y')
```


- #584 Find Customer Referee [link](https://leetcode.com/problems/find-customer-referee/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select name
from Customer
where (Customer.referee_id is Null) or (Customer.referee_id != 2)
```


- #595 Big Countries [link](https://leetcode.com/problems/big-countries/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select name, population, area
from World
where (World.area >= 3000000) or (World.population >= 25000000)
```


- #1148 Article Views I [link](https://leetcode.com/problems/article-views-i/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select distinct author_id as 'id'
from Views
where Views.author_id = Views.viewer_id
order by author_id asc
```


- #1683 Invalid Tweets [link](https://leetcode.com/problems/invalid-tweets/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select tweet_id
from Tweets
where char_length(Tweets.content) > 15
```
