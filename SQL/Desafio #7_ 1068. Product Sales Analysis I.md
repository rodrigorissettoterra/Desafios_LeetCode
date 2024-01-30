<h1>1068. Product Sales Analysis I</h1>
&nbsp;
<h2>Problema</h2>
<div class="xFUwe" data-track-load="description_content">
<div class="xFUwe" data-track-load="description_content">

Table: <code>Sales</code>
<pre>+-------------+-------+
| Column Name | Type  |
+-------------+-------+
| sale_id     | int   |
| product_id  | int   |
| year        | int   |
| quantity    | int   |
| price       | int   |
+-------------+-------+
(sale_id, year) is the primary key (combination of columns with unique values) of this table.
product_id is a foreign key (reference column) to <code>Product</code> table. Each row of this table shows a sale on the product product_id in a certain year. Note that the price is per unit.</pre>
&nbsp;

Table: <code>Product</code>
<pre>+--------------+---------+
| Column Name  | Type    |
+--------------+---------+
| product_id   | int     |
| product_name | varchar |
+--------------+---------+
product_id is the primary key (column with unique values) of this table.
Each row of this table indicates the product name of each product.
</pre>
&nbsp;

Write a solution to report the <code>product_name</code>, <code>year</code>, and <code>price</code> for each <code>sale_id</code> in the <code>Sales</code> table.

Return the resulting table in <strong>any order</strong>.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
Sales table:
+---------+------------+------+----------+-------+
| sale_id | product_id | year | quantity | price |
+---------+------------+------+----------+-------+ 
| 1       | 100        | 2008 | 10       | 5000  |
| 2       | 100        | 2009 | 12       | 5000  |
| 7       | 200        | 2011 | 15       | 9000  |
+---------+------------+------+----------+-------+
Product table:
+------------+--------------+
| product_id | product_name |
+------------+--------------+
| 100        | Nokia        |
| 200        | Apple        |
| 300        | Samsung      |
+------------+--------------+
<strong>Output:</strong> 
+--------------+-------+-------+
| product_name | year  | price |
+--------------+-------+-------+
| Nokia        | 2008  | 5000  |
| Nokia        | 2009  | 5000  |
| Apple        | 2011  | 9000  |
+--------------+-------+-------+
<strong>Explanation:</strong> 
From sale_id = 1, we can conclude that Nokia was sold for 5000 in the year 2008.
From sale_id = 2, we can conclude that Nokia was sold for 5000 in the year 2009.
From sale_id = 7, we can conclude that Apple was sold for 9000 in the year 2011.
</pre>
</div>
</div>
<h2>Solução:</h2>
<div>
<div>
<div>
<div>
<div>
<div></div>
</div>
</div>
</div>
</div>
</div>
<div>
<div>
<div>
<div>select p.product_name, s.year, s.price</div>
<div>from product p LEFT JOIN sales s</div>
<div>on (p.product_id = s.product_id)</div>
<div>where s.year IS NOT NULL</div>
</div>
