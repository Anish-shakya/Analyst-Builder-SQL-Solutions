![Alt text](image.png)

```sql
SELECT TOP 1 *,
(CAST(car_price AS DECIMAL(10,2))-CAST(production_cost AS DECIMAL(10,2))) 
* CAST(cars_sold AS DECIMAL(10,2)) AS Profit
FROM tesla_models
ORDER BY profit DESC
```

![Alt text](image-1.png)

```sql
SELECT * 
FROM patients
WHERE age > 50 AND cholesterol >= 240 AND weight >=200
ORDER BY cholesterol DESC
```

![Alt text](image-2.png)
```sql
SELECT COUNT(*) as total_customer
FROM customers
WHERE age>65 or total_purchase > 200    
```
![Alt text](image-3.png)

```sql
SELECT store_id , ROUND(AVG(CAST(revenue AS DECIMAL(10,2))),2)AS Average_Revenue
FROM stores
GROUP BY store_id
HAVING AVG(revenue) > 1000000
ORDER BY store_id


```