# mockdata
create mock data in json form according to data structure define.

## background and idea

In frontend development, we need only data structure and REST api to support our progress
on development. But waiting the guys who own backend service is too slow. So we need some 
ways to mock REST api behavior and data.

We can predefined the data structure in json. And then create mock data according to data 
structure. we can store mock data as json file with specify path and file name. And provide
a common CRUD api to support development.
For example, we need process and display students information to end user. And every student
is indentified by No. we can store each student mock data in a path like this "{somedir}/students/{NO.}.json".

So, it is easy to support request like:
- GET /students get all students
- GET /students/{NO} get a student data
....

For these, we only need to do is map request to file i/o.
