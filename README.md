# Database 101
## Introduction
This is the course materials for Database 101 in UiS.

## Prerequisite
- Knowing basic query in MySQL.
- Understanding the logic between application and database

## Requirement
- UiS Linux server

## Tasks

You built the Instagram kind of application. There are three tables in this database.
- users: u_id, u_name, u_email, u_created_time, u_created_timestamp, u_latitude, u_longitude
- posts: p_id, p_title, p_content, p_u_id, p_created_time, p_created_timestamp, p_latitude, p_longitude
- comments: c_id, c_p_id, c_u_id, comment, c_created_time, c_created_timestamp



### Task 1
Return the posts with its authors name. The order of contents should be descending by the post's created time.
### Task 2
The marketing manager wants you to provide the monthly statistics of your application.
- Return the number of posts per months, and the order should be descending by the created time.

### Task 3
You added the `u_created_time` field later, therefore, early users are missing `u_created_time` value. Fill up this field using `u_created_timestamp`.

### Task 4
You forgot to create the `likes` tables. Build a `likes` table corresponding to the posts table.

### Task 5
Return the posts with its authors name and the number of comments. The order of contents should be descending by the number of comments. (It should be able to show the posts have no comments as well.)

### Task 6
You want to develop a notification function. The notification will be sent when someone post or comment (regardless of whose content is). Return the posts and comments together with its `created_time` descending order.

### Task 7
You want to add your own feature to be different with Instagram. You want to show users in the order of posts close to the user's distance. Return the posts for `u_id = "3"` with posts' distance.
