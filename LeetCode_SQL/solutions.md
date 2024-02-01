- #1757 Recyclable and Low Fat Products [link](https://leetcode.com/problems/recyclable-and-low-fat-products/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select product_id
from Products
where (Products.low_fats = 'Y') and (Products.recyclable = 'Y')
```


