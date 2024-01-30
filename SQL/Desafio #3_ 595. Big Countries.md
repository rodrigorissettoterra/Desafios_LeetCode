<h1>595. Big Countries</h1>
&nbsp;
<h2>Problema</h2>
<div class="xFUwe" data-track-load="description_content">

Table: <code>World</code>
<pre>+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| name        | varchar |
| continent   | varchar |
| area        | int     |
| population  | int     |
| gdp         | bigint  |
+-------------+---------+
name is the primary key (column with unique values) for this table.
Each row of this table gives information about the name of a country, the continent to which it belongs, its area, the population, and its GDP value.
</pre>
&nbsp;

A country is <strong>big</strong> if:
<ul>
 	<li>it has an area of at least three million (i.e., <code>3000000 km<sup>2</sup></code>), or</li>
 	<li>it has a population of at least twenty-five million (i.e., <code>25000000</code>).</li>
</ul>
Write a solution to find the name, population, and area of the <strong>big countries</strong>.

Return the result table in <strong>any order</strong>.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
World table:
+-------------+-----------+---------+------------+--------------+
| name        | continent | area    | population | gdp          |
+-------------+-----------+---------+------------+--------------+
| Afghanistan | Asia      | 652230  | 25500100   | 20343000000  |
| Albania     | Europe    | 28748   | 2831741    | 12960000000  |
| Algeria     | Africa    | 2381741 | 37100000   | 188681000000 |
| Andorra     | Europe    | 468     | 78115      | 3712000000   |
| Angola      | Africa    | 1246700 | 20609294   | 100990000000 |
+-------------+-----------+---------+------------+--------------+
<strong>Output:</strong> 
+-------------+------------+---------+
| name        | population | area    |
+-------------+------------+---------+
| Afghanistan | 25500100   | 652230  |
| Algeria     | 37100000   | 2381741 |
+-------------+------------+---------+
</pre>
</div>
</br>
<h2>Solução:</h2>
<div>
<div>
<div>
<div>
<div>select name, population, area from world</div>
<div>where (</div>
<div>    (area&gt;=3000000) OR</div>
<div>    (population&gt;=25000000)</div>
<div>)</div>
</div>
</div>
<div></div>
</div>
</div>
