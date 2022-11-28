# 22.11.2022 SQL ÖDEV

## * Hangi Kategoride kaç ürün vardır(Inner Join)
`select ca.name, count(pr.id) as adet from products pr
inner join product_categories pc
on pr.id = pc.product_id
inner join categories ca
on ca.id=pc.category_id
group by ca.name
order by adet desc`

<p  align="center">
<img src="kategori.png" width=40% height=40%>
  </p>

## * --product tablosuna ürün eklemek
`INSERT INTO products(name,stock,unit_price)
VALUES('masa',5,200)`

## * --isme göre masa isimli ürün stok durumunu update edildi

`UPDATE products
SET stock=30
WHERE products."name"='masa'`

  
## * --outer join

`SELECT * from product_categories pc
full outer join products p 
on pc.product_id= p.id`

<p  align="center">
<img src="Full outer.png" width=40% height=40%>
  </p>
  
## * Bütün kullanıcılar ve siparişler (RIGHT JOIN)
`Select * from orders
right join customer on orders.customer_id = customer.id`

<p  align="center">
<img src="28.11.22_SQL_Ödev/r6.png" width=60% height=60%>
  </p>
  
## * Renklerin ve ürünlerin hepsini (FULL OUTER JOIN)
`Select color.name as "Renk", product.name "Ürün" from product
full outer join color on product.color_id = color.id
order by product.name`

<p  align="center">
<img src="28.11.22_SQL_Ödev/r7.png" width=40% height=40%>
  </p>
