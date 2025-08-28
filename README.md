# Atividades-SQL-BEECROWD
Atividades realizadas no site da beecrowd para aperfeicoamento das habilidades em SQL
## Desafios Nivel 1 ✔
### Desafio 2603- Endereço dos clientes 😃
<img width="1080" height="308" alt="Image" src="https://github.com/user-attachments/assets/a829782a-9e78-4dad-a8b7-997f0394962c" />

``` sql
select name, street

from 
    customers
where
    city='Porto Alegre'
```
## Desafio 2607 - Cidades em Ordem Alfabética 😎
<img width="1081" height="306" alt="Image" src="https://github.com/user-attachments/assets/1e3e777f-eda9-4865-a40d-0c3cd92dc9b1" />

``` sql
Select 
    city
from 
    providers
order by city asc
```
### Desafio 2608 - Maior e Menor Preço 😁
<img width="1086" height="307" alt="Image" src="https://github.com/user-attachments/assets/578c003f-ce9f-4e35-a8d9-9dfb427328c2" />

``` sql
select
max(price),min(price)
from products;
```
## Desafio 2615- Expandindo Negocio 👏
<img width="1080" height="307" alt="Image" src="https://github.com/user-attachments/assets/1086f045-3d4e-4faf-8e20-74685cb78303" />

``` sql
select 
     city 
from
    customers
group by
    city;
```

## Desafio 2617 - Fornecedor Ajax SA 🌹
<img width="1076" height="294" alt="Image" src="https://github.com/user-attachments/assets/60b7f78a-444f-497d-aa46-e999952265d0" />

``` sql
SELECT 
    p.name AS product_name,
    pr.name AS provider_name
FROM 
    products p
JOIN 
    providers pr
    ON p.id_providers = pr.id
WHERE 
    pr.name = 'Ajax SA';
```

## Desafios Nivel 2 ✔
### Desafio 2613 - Filmes em Promoção 💋
<img width="1086" height="453" alt="Image" src="https://github.com/user-attachments/assets/ec86c967-ff3d-4e7f-b8fd-fcd36bdf7653" />

``` sql
select
    a.id,
    a.name
from movies a
join prices ar
on a.id_prices = ar.id
where ar.value < 2.00;
```

## Desafio 2619 - Super Luxo 🐱‍🏍
<img width="1088" height="306" alt="Image" src="https://github.com/user-attachments/assets/99d409f4-ca4d-4be9-bae0-71f1c843079f" />

``` sql
select
a.name as product_name,
ar.name as provider_name,
a.price
from 
	products a
join 
	providers ar
on 
	a.id_providers = ar.id
join 
	categories c
on 
	a.id_categories = c.id
where 
	a.price > 1000
	and c.name = 'Super Luxury';
```

## Desafios Nivel 3 ✔
### Desafio 2606 - Categorias 👌
<img width="1086" height="311" alt="Image" src="https://github.com/user-attachments/assets/a6ced2ea-1007-4522-91b3-c047e72c1a9d" />

``` sql
select
p.id,
p.name
from products p
join categories c
on p.id_categories = c.id
where c.name like 'super%';
```

## Desafio 2621 - Quantidades Entre 10 e 20 🤞
<img width="1086" height="320" alt="Image" src="https://github.com/user-attachments/assets/48eee679-b441-4d62-8f9f-36c51998a9d8" />

``` sql
select
p.name
from products p
join providers pr
on p.id_providers = pr.id
where p.amount between 10 and 20
and pr.name like 'P%';
```

## Desafio Nivel 5 ✔
### Desafio 2616 - Nenhuma locação ✨
<img width="1086" height="305" alt="Image" src="https://github.com/user-attachments/assets/389a427a-b7e5-46c2-b1bb-295493a72cd7" />

``` sql
SELECT
c.id,
c.name
FROM
customers c
LEFT JOIN
locations l
ON
c.id = l.id_customers
WHERE
l.id_customers IS NULL
ORDER BY
c.id;
```
