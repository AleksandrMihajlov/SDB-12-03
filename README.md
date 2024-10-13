# SDB-12-03
SQL. Часть 1 - Aleksandr Mihajlov SYS34  
  
### Задание 1  
  
Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.  
  
```sql
select district from sakila.address
where district like 'K%a' and district not like '% %'
```
![alt text](https://github.com/AleksandrMihajlov/SDB-12-03/blob/main/1.png)  
  
### Задание 2  
  
Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.  
  
```sql  
select * from sakila.payment
where payment_date between '2005-06-15 00:00:00' and '2005-06-18 23:59:59' and amount >10
```  
![alt text](https://github.com/AleksandrMihajlov/SDB-12-03/blob/main/2.png)  
  
### Задание 3  
  
```sql
select * from sakila.rental order by rental_date desc limit 5
```  
![alt text](https://github.com/AleksandrMihajlov/SDB-12-03/blob/main/3.png)  
  
### Задание 3  
  
```sql
select replace (lower(first_name), 'll' , 'pp') , lower(last_name) , active
from sakila.customer
where first_name = 'Kelly' or first_name = 'Willie'
```
![alt text](https://github.com/AleksandrMihajlov/SDB-12-03/blob/main/4.png)