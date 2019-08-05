# Database 101
## Introduction
This is the course materials for Database 101 in UiS.

## Prerequisite
- Knowing basic query in MySQL.
- Understanding the logic between application and database

## Requirement
- UiS Linux server with MySQL

## Tasks

You built the Instagram kind of application. There are three tables in the database (one is not created yet).
- users: u_id, u_name, u_email, u_created_time, u_created_timestamp, u_latitude, u_longitude
- posts: p_id, p_title, p_content, p_u_id, p_created_time, p_created_timestamp, p_latitude, p_longitude
- comments: c_id, c_p_id, c_u_id, comment, c_created_time, c_created_timestamp
- likes (not created yet): l_id, l_p_id, l_u_id, l_created_time, l_created_timestamp

Complete the below tasks using a single query (one-time execution).



### Task 1
Return the posts, including its author's name. It should be descending order by the post's created time.

Sample Output
'''
159	Zadok Rabinowitz	A man's dreams are an index to his greatness.	4	2019-01-21 20:41:23	1548099683	-87.9016	-96.2723	sadcat660
334	Confucius	What you do not want done to yourself, do not do to others.	8	2019-01-25 13:15:32	1548418532	-17.011499999999998	88.5789	crazyelephant206
418	Mary Almanac	Who we are never changes. Who we think we are does.	6	2019-01-26 13:55:04	1548507304	32.0418	-155.908	silverzebra412
350	William Shakespeare	It is not in the stars to hold our destiny but in ourselves.	10	2019-01-26 13:56:53	1548507413	17.7112	155.637	silverfish931
...
'''

### Task 2
The marketing manager wants you to provide the monthly statistics of your application. Return the number of posts per months, and it should be descending order by the month.

### Task 3
You added the `u_created_time` field later, therefore, early users are missing `u_created_time` value. Fill up this field using `u_created_timestamp`.

### Task 4
You forgot to create the `likes` table. Build a `likes` table.

### Task 5
(extended from task1) Return the posts with their author's name and the number of comments. The order of contents should be descending by the number of comments. (It should be able to show the posts have no comments as well.)

### Task 6
You want to develop a notification function. The notification will be sent when someone post or comment (regardless of whose content is). Return the posts and comments together with its `created_time` descending order.

### Task 7
You want to add your own feature to be different from Instagram. You want to show users in the order of posts close to the user's distance. Return the posts from `latitude=67.157, longitude=7.4002` where distance is less than 1,000km.


## Helpful Resource

- [w3school](https://www.w3schools.com/sql/default.asp)
