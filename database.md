# DATABASE

## SQL Commands

| description | command  | 
--- | --- |
|Login|sql -U [username] -h localhost -D [databasename]|
|Comment in SQL|--text|
|List tables|\d|
|List databases|\l|
|List scripts|\i|
|List users|\du|

### USER

| description | command  | 
--- | --- |
|Login as user|\c [databasename] [usename]|
|Create user|create user [name] password ['password'];|
|Modify user password|alter user [name] with password ['password']; |
|Delete user|drop user [name];|

### DATABASE

| description | command  | 
--- | --- |
|Create database|create database [name];|
|Acess database|\c [name]| 
|Delete database|drop database [name];

### TABLE

| description | command  | 
--- | --- |
|Create table|create table if not exists [name] (att; att; const;)|
|Alter table|??|
|Delete table|drop table [name];|
|Insert value|insert into [tablename] (attributes) values (values);|

### DATA QUERY

| description | command |
--- | --- |
|Check value with condition|select [attribute] from [tablename] where [condition];<br> cond like (value) = equal (value) <br>cond in (value1, value2) = value1 or value2 <br>cond between (value1, value2) = value1 to value2 <br>|
|Check value ordered|select [attribute] from [tablename] order by [attribute asc/desc];|
|Check value with nickname|select [tablenick.attribute];|
|Upper and lowercase|lower/upper()|
|Get first or last char|left/right(string, #char) or left(name,4)|
|Show text|select case when [condition] then [text], when (...), end case;|
|Placeholder title| select [attribute] as [tempname];| 
