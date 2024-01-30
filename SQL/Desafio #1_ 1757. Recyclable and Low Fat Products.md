<h1>1757. Recyclable and Low Fat Products</h1>

<h2>Problema:</h2>
<div class="xFUwe" data-track-load="description_content">

Table: <code>Products</code>
<pre>+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| product_id  | int     |
| low_fats    | enum    |
| recyclable  | enum    |
+-------------+---------+
product_id is the primary key (column with unique values) for this table.
low_fats is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
recyclable is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.</pre>
&nbsp;

Write a solution to find the ids of products that are both low fat and recyclable.

Return the result table in <strong>any order</strong>.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
Products table:
+-------------+----------+------------+
| product_id  | low_fats | recyclable |
+-------------+----------+------------+
| 0           | Y        | N          |
| 1           | Y        | Y          |
| 2           | N        | Y          |
| 3           | Y        | Y          |
| 4           | N        | N          |
+-------------+----------+------------+
<strong>Output:</strong> 
+-------------+
| product_id  |
+-------------+
| 1           |
| 3           |
+-------------+
<strong>Explanation:</strong> Only products 1 and 3 are both low fat and recyclable.
</pre>
</div>
<h2></h2>
<h2>Solução:</h2>
<div>
<div>select product_id from Products</div>
<div>where (low_fats='Y' AND recyclable='Y')</div>
</div>
<div></div>
<div></div>
