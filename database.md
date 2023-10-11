# DATABASE
We are learning PSQL - PostgreSQL. It should be installed first before being used in the CMD. Postgre is a variation of SQL, and after learning it, we should be able to work with any SQL-type database, as the concepts are almost the same.

## SQL Commands
After logging in, we should see a pattern like **postgre#=** in the command line, where:
- **postgre** it's the database name;
- **#** is a character representing the authority of the user ('#' for super users, '/' for normal users);
- **=** is a character representing the command status ('=' means idling and '-' means waiting for a command).

| description | command  | 
--- | --- |
|Login|sql -U [username] -h localhost -D [databasename]|
|Comment in SQL|--text|
|List tables|\d|
|List databases|\l|
|List scripts|\i|
|List users|\du|

### USER
Users are separated by permission levels, like super user or normal user.<br>
The standart "postgre" user with "postgre" password is a super user. Remember to always change its password when setting up a database, for security reasons.

| description | command  | 
--- | --- |
|Login as user|\c [databasename] [usename]|
|Create user|create user [name] password ['password'];|
|Modify user password|alter user [name] with password ['password']; |
|Delete user|drop user [name];|

### DATABASE
Postgre has a standart "postgre" database. Remember to always log into your desired database before you start making changes.

| description | command  | 
--- | --- |
|Create database|create database [name];|
|Acess database|\c [name]| 
|Delete database|drop database [name];

### TABLE
Tables are our main tool in SQL. That's where we store and organize our data. 

| description | command  | 
--- | --- |
|Create table|create table if not exists [tablename] (att; att; const;)|
|Alter table|alter table [tablename] [action] (...)<br> - add/drop/alter column [columnname]|
|Delete table|drop table [tablename];|
|Insert value|insert into [tablename] (attributes) values (values);|

### DATA MANIPULATION

| description | command |
--- | --- |
|Upper and lowercase|lower/upper()|
|Get first or last char|left/right(string, #char) or left(name,4)|
|Limit results| (...) limit [number];|

### SELECT
Select is the base search command in PSQL.
- Highly costumizable, as it is our base tool.
- We can nest selects to create "sub-queries".

| description | command |
--- | --- |
|Basic select|select [attribute] from [tablename] where [condition];<br> cond like (value) = equal (value) <br>cond in (value1, value2) = value1 or value2 <br>cond between (value1, value2) = value1 to value2 <br>|
|Check value ordered|select [attribute] from [tablename] order by [attribute asc/desc];|
|Check value with nickname|select [tablenick.attribute];|
|Show text|select case when [condition] then [text], when (...), end case;|
|Placeholder title| select [attribute] as [tempname];| 

### JOIN
Join allow us to access and relate multiple tables in a single search. The left join is used in 99.8% of cases, with inner join comming second. Right and full join are barely used, especially because right join can be used as left join if we invert the tables.
- Left join returns the common attributes + the left table attributes.
- Right join does the same as left join, but returns the right table attributes instead of the left ones.
- Inner join returns only the common set.
- Full join returns all from both tables as well as the common set.

| description | command |
--- | --- |
|Left join|(...) from [tablename] left join [tablename] on [condition] (...)|
|Right join|(...) from [tablename] right join [tablename] on [condition] (...)|
|Inner join|(...) from [tablename] inner join [tablename] on [condition] (...)|
|Full join|(...) from [tablename] full join [tablename] on [condition] (...)|
