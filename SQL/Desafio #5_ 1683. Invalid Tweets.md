<h1>1683. Invalid Tweets</h1>
&nbsp;
<h2>Problema</h2>
<div class="xFUwe" data-track-load="description_content">
<div class="xFUwe" data-track-load="description_content">
<div class="xFUwe" data-track-load="description_content">

Table: <code>Tweets</code>
<pre>+----------------+---------+
| Column Name    | Type    |
+----------------+---------+
| tweet_id       | int     |
| content        | varchar |
+----------------+---------+
tweet_id is the primary key (column with unique values) for this table.
This table contains all the tweets in a social media app.
</pre>
&nbsp;

Write a solution to find the IDs of the invalid tweets. The tweet is invalid if the number of characters used in the content of the tweet is <strong>strictly greater</strong> than <code>15</code>.

Return the result table in <strong>any order</strong>.

The result format is in the following example.

&nbsp;

<strong class="example">Example 1:</strong>
<pre><strong>Input:</strong> 
Tweets table:
+----------+----------------------------------+
| tweet_id | content                          |
+----------+----------------------------------+
| 1        | Vote for Biden                   |
| 2        | Let us make America great again! |
+----------+----------------------------------+
<strong>Output:</strong> 
+----------+
| tweet_id |
+----------+
| 2        |
+----------+
<strong>Explanation:</strong> 
Tweet 1 has length = 14. It is a valid tweet.
Tweet 2 has length = 32. It is an invalid tweet.
</pre>
</div>
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
<div>
<div>SELECT tweet_id</div>
<div>FROM Tweets</div>
<div>WHERE CHAR_LENGTH(content) &gt; 15;</div>
</div>
</div>
