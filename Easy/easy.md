![Alt text](image.png)

```sql
SELECT TOP 1 *,
(CAST(car_price AS DECIMAL(10,2))-CAST(production_cost AS DECIMAL(10,2))) 
* CAST(cars_sold AS DECIMAL(10,2)) AS Profit
FROM tesla_models
ORDER BY profit DESC
```