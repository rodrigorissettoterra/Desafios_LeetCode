<h1>1378. Replace Employee ID With The Unique Identifier</h1>
&nbsp;
<h2>Problema</h2>
<div class="xFUwe" data-track-load="description_content">

Table: <code>Employees</code>
<pre>+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| id            | int     |
| name          | varchar |
+---------------+---------+
id is the primary key (column with unique values) for this table.
Each row of this table contains the id and the name of an employee in a company.
</pre>
&nbsp;

Table: <code>EmployeeUNI</code>
<pre>+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| id            | int     |
| unique_id     | int     |
+---------------+---------+
(id, unique_id) is the primary key (combination of columns with unique values) for this table.
Each row of this table contains the id and the corresponding unique id of an employee in the company.
</pre>
&nbsp;

Write a solution to show the <strong>unique ID </strong>of each user, If a user does not have a unique ID replace just show <code>null</code>.

Return the result table in <strong>any</strong> order.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
Employees table:
+----+----------+
| id | name     |
+----+----------+
| 1  | Alice    |
| 7  | Bob      |
| 11 | Meir     |
| 90 | Winston  |
| 3  | Jonathan |
+----+----------+
EmployeeUNI table:
+----+-----------+
| id | unique_id |
+----+-----------+
| 3  | 1         |
| 11 | 2         |
| 90 | 3         |
+----+-----------+
<strong>Output:</strong> 
+-----------+----------+
| unique_id | name     |
+-----------+----------+
| null      | Alice    |
| null      | Bob      |
| 2         | Meir     |
| 3         | Winston  |
| 1         | Jonathan |
+-----------+----------+
<strong>Explanation:</strong> 
Alice and Bob do not have a unique ID, We will show null instead.
The unique ID of Meir is 2.
The unique ID of Winston is 3.
The unique ID of Jonathan is 1.
</pre>
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
<div>SELECT eu.unique_id, e.name</div>
<div>FROM Employees e</div>
<div>LEFT JOIN EmployeeUNI eu</div>
<div>ON e.id = eu.id</div>
