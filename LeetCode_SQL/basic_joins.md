- #1378 Replace Employee ID With The Unique Identifier [link](https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
SELECT EmployeeUNI.unique_id, Employees.name
FROM Employees
LEFT JOIN EmployeeUNI on Employees.id = EmployeeUNI.id
```


- #1068 Product Sales Analysis I [link](https://leetcode.com/problems/product-sales-analysis-i/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select Product.product_name, Sales.year, Sales.price
from Sales
left join Product on Sales.product_id = Product.product_id
```


- #1581 Customer Who Visited but Did Not Make Any Transactions [link](https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select Visits.customer_id, count(Visits.visit_id) AS count_no_trans 
from Visits
left join Transactions on Visits.visit_id = Transactions.visit_id
where Transactions.transaction_id is null
group by Visits.customer_id
```


- #197 Rising Temperature [link](https://leetcode.com/problems/rising-temperature/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select w1.id
from Weather w1, Weather w2
where DATEDIFF(w1.recordDate, w2.recordDate) = 1 and w1.temperature > w2.temperature;
```


- #1661 Average Time of Process per Machine [link](https://leetcode.com/problems/average-time-of-process-per-machine/description/?envType=study-plan-v2&envId=top-sql-50)
```sql
select a1.machine_id, round(avg(a2.timestamp-a1.timestamp), 3) as processing_time 
from Activity a1
join Activity a2 
on a1.machine_id=a2.machine_id and a1.process_id=a2.process_id
and a1.activity_type='start' and a2.activity_type='end'
group by a1.machine_id
```




