<h1>1148. Article Views I</h1>
&nbsp;
<h2>Problema</h2>
<div class="xFUwe" data-track-load="description_content">
<div class="xFUwe" data-track-load="description_content">

Table: <code>Views</code>
<pre>+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| article_id    | int     |
| author_id     | int     |
| viewer_id     | int     |
| view_date     | date    |
+---------------+---------+
There is no primary key (column with unique values) for this table, the table may have duplicate rows.
Each row of this table indicates that some viewer viewed an article (written by some author) on some date. 
Note that equal author_id and viewer_id indicate the same person.
</pre>
&nbsp;

Write a solution to find all the authors that viewed at least one of their own articles.

Return the result table sorted by <code>id</code> in ascending order.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
Views table:
+------------+-----------+-----------+------------+
| article_id | author_id | viewer_id | view_date  |
+------------+-----------+-----------+------------+
| 1          | 3         | 5         | 2019-08-01 |
| 1          | 3         | 6         | 2019-08-02 |
| 2          | 7         | 7         | 2019-08-01 |
| 2          | 7         | 6         | 2019-08-02 |
| 4          | 7         | 1         | 2019-07-22 |
| 3          | 4         | 4         | 2019-07-21 |
| 3          | 4         | 4         | 2019-07-21 |
+------------+-----------+-----------+------------+
<strong>Output:</strong> 
+------+
| id   |
+------+
| 4    |
| 7    |
+------+
</pre>
</div>
</div>
<h2></h2>
<h2>Solução:</h2>
<div>
<div>
<div>
<div>
<div>
<div>select distinct author_id as id from Views</div>
<div>where (author_id = viewer_id)</div>
<div>order by id</div>
</div>
</div>
</div>
</div>
</div>
