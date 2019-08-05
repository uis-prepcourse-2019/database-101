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

### Task 0
Import `group-task.sql` into your database and set up the dataset.


### Task 1
Return the posts, including its author's name. It should be descending order by the post's created time.

Sample Output
```
159	Zadok Rabinowitz	A man's dreams are an index to his greatness.	4	2019-01-21 20:41:23	1548099683	-87.9016	-96.2723	sadcat660
334	Confucius	What you do not want done to yourself, do not do to others.	8	2019-01-25 13:15:32	1548418532	-17.011499999999998	88.5789	crazyelephant206
418	Mary Almanac	Who we are never changes. Who we think we are does.	6	2019-01-26 13:55:04	1548507304	32.0418	-155.908	silverzebra412
350	William Shakespeare	It is not in the stars to hold our destiny but in ourselves.	10	2019-01-26 13:56:53	1548507413	17.7112	155.637	silverfish931
...
```

### Task 2
The marketing manager wants you to provide the monthly statistics of your application. Return the number of posts per months, and it should be descending order by the month.

Sample Output
```
8	20
7	77
6	85
5	85
4	66
3	80
2	65
1	22
```
### Task 3
You added the `u_created_time` field later, therefore, early users are missing `u_created_time` value. Fill up this field using `u_created_timestamp`.

### Task 4
You forgot to create the `likes` table. Build a `likes` table.

### Task 5
(extended from task1) Return the posts with their author's name and the number of comments. The order of contents should be descending by the number of comments. (It should be able to show the posts have no comments as well.)

Sample Output
```
159	Zadok Rabinowitz	A man's dreams are an index to his greatness.	4	2019-01-21 20:41:23	1548099683	-87.9016	-96.2723	sadcat660	0
334	Confucius	What you do not want done to yourself, do not do to others.	8	2019-01-25 13:15:32	1548418532	-17.011499999999998	88.5789	crazyelephant206	1
418	Mary Almanac	Who we are never changes. Who we think we are does.	6	2019-01-26 13:55:04	1548507304	32.0418	-155.908	silverzebra412	0
350	William Shakespeare	It is not in the stars to hold our destiny but in ourselves.	10	2019-01-26 13:56:53	1548507413	17.7112	155.637	silverfish931	0
259	Tim Menchen	To dream of the person you would like to be is to waste the person you are.	6	2019-01-26 16:19:04	1548515944	36.2418	-163.208	silverzebra412	4
```
### Task 6
You want to develop a notification function. The notification will be sent when someone post or comment (regardless of whose content is). Return the posts and comments together with its `created_time` descending order.

Sample Output
```
154	It is easier to live through someone else than to become complete yourself.	2019-08-20 04:16:07	3	lazyduck547	comment
286	Cherish your visions and your dreams as they are the children of your soul, the blueprints of your ultimate achievements.	2019-08-18 07:28:12	32	purpleswan939	comment
413	When we feel love and kindness toward others, it not only makes others feel loved and cared for, but it helps us also to develop inner happiness and peace.	2019-08-18 04:16:07	106	blacktiger871	comment
463	Judge nothing, you will be happy. Forgive everything, you will be happier. Love everything, you will be happiest.	2019-08-16 00:16:12	148	heavyleopard119	comment
314	Life isn't about finding yourself. Life is about creating yourself.	2019-08-15 17:55:47	62	yellowfrog723	comment
55	Never bend your head. Always hold it high. Look the world right in the eye.	2019-08-14 16:40:49	193	goldenfish505	comment
237	Don't judge each day by the harvest you reap but by the seeds you plant.	2019-08-14 08:40:07	200	sadladybug720	comment
488	Better than a thousand hollow words is one word that brings peace.	2019-08-13 22:57:38	148	heavyleopard119	comment
220	I have always thought the actions of men the best interpreters of their thoughts.	2019-08-12 20:09:38	199	heavygoose557	comment
431	Gratitude is riches. Complaint is poverty.	2019-08-12 01:07:47	197	crazyzebra251	comment
54	Benjamin Spock	2019-08-12 00:57:38	199	heavygoose557	post
437	Maya Angelou	2019-08-11 23:04:07	200	sadladybug720	post
290	If you correct your mind, the rest of your life will fall into place.	2019-08-11 16:40:12	198	tinyswan576	comment
...
```
### Task 7
You want to add your own feature to be different from Instagram. You want to show users in the order of posts close to the user's distance. Return the posts from `latitude=67.157, longitude=7.4002` where distance is less than 1,000km.

Sample Output
```
343	Richard Bach	If you love someone, set them free. If they come back they're yours; if they don't they never were.	127	2019-05-26 09:35:33	1558856133	66.5775	7.354100000000001	64.46891679964803
90	Lao Tzu	He who talks more is sooner exhausted.	57	2019-03-19 06:46:42	1552974402	68.1608	3.5324	197.89707500577046
11	Man Ray	It has never been my object to record my dreams, just to realize them.	127	2019-06-01 19:11:33	1559409093	65.8775	11.0541	215.46887290864635
157	Saul Alinsky	As an organizer I start from where the world is, as it is, not as I would like it to be.	57	2019-03-23 23:34:42	1553380482	69.2608	-1.8676	447.7444566068912
59	Lewis Cass	People may doubt what you say, but they will believe what you do.	127	2019-05-29 09:35:33	1559115333	61.9775	16.054100000000002	707.4964271411941
183	Buddha	We are what we think. All that we are arises with our thoughts. With our thoughts, we make the world.	57	2019-03-15 01:58:42	1552611522	73.96079999999999	4.3324	764.7698872392185
37	Wayne Dyer	You'll see it when you believe it.	57	2019-03-17 18:46:42	1552844802	74.5608	-1.0676	877.2085009314773
7	Naguib Mahfouz	You can tell whether a man is clever by his answers. You can tell whether a man is wise by his questions.	57	2019-03-23 04:22:42	1553311362	75.2608	3.9324	909.238400207677
468	Socrates	Wisdom begins in wonder.	57	2019-03-14 06:46:42	1552542402	75.1608	1.6324	912.7242365366025
285	Thich Nhat Hanh	The most precious gift we can offer anyone is our attention. When mindfulness embraces those we love, they will bloom like flowers.	2	2019-01-26 23:53:39	1548543219	66.0529	-13.2291	914.7153119616595
```

## Helpful Resource

- [w3school](https://www.w3schools.com/sql/default.asp)
