# Atividades-SQL-BEECROWD
Atividades realizadas no site da beecrowd para aperfeicoamento das habilidades em SQL
## Desafios Nivel 1
### Desafio 2603- Endereço dos clientes
<img width="1080" height="308" alt="Image" src="https://github.com/user-attachments/assets/a829782a-9e78-4dad-a8b7-997f0394962c" />

``` sql
select name, street

from 
    customers
where
    city='Porto Alegre'
```
## Desafio 2607 - Cidades em Ordem Alfabética
<img width="1081" height="306" alt="Image" src="https://github.com/user-attachments/assets/1e3e777f-eda9-4865-a40d-0c3cd92dc9b1" />

``` sql
Select 
    city
from 
    providers
order by city asc
```
### Desafio 2608 - Maior e Menor Preço
<img width="1080" height="308" alt="Image" src="https://github.com/user-attachments/assets/a829782a-9e78-4dad-a8b7-997f0394962c" />

``` sql
select
max(price),min(price)
from products;
```
## Desafio 2615- Expandindo Negocio
<img width="1081" height="306" alt="Image" src="https://github.com/user-attachments/assets/1e3e777f-eda9-4865-a40d-0c3cd92dc9b1" />

``` sql
select 
     city 
from
    customers
group by
    city;
```
## Desafio 2617 - Fornecedor Ajax SA
<img width="1081" height="306" alt="Image" src="https://github.com/user-attachments/assets/1e3e777f-eda9-4865-a40d-0c3cd92dc9b1" />

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
