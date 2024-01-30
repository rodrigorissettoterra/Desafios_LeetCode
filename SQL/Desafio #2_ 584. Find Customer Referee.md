<h1>584. Find Customer Referee</h1>
&nbsp;
<h2>Problema</h2>
<div class="xFUwe" data-track-load="description_content">

Table: <code>Customer</code>
<pre>+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| id          | int     |
| name        | varchar |
| referee_id  | int     |
+-------------+---------+
In SQL, id is the primary key column for this table.
Each row of this table indicates the id of a customer, their name, and the id of the customer who referred them.
</pre>
&nbsp;

Find the names of the customer that are <strong>not referred by</strong> the customer with <code>id = 2</code>.

Return the result table in <strong>any order</strong>.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
Customer table:
+----+------+------------+
| id | name | referee_id |
+----+------+------------+
| 1  | Will | null       |
| 2  | Jane | null       |
| 3  | Alex | 2          |
| 4  | Bill | null       |
| 5  | Zack | 1          |
| 6  | Mark | 2          |
+----+------+------------+
<strong>Output:</strong> 
+------+
| name |
+------+
| Will |
| Jane |
| Bill |
| Zack |
+------+
</pre>
</div>
<h2></h2>
<h2>Solução:</h2>
<div>
<div>
<div>select name from Customer</div>
<div>where (referee_id &lt;&gt;2 or referee_id is null)</div>
</div>
</div>
<div></div>
<div></div>
<div></div>
