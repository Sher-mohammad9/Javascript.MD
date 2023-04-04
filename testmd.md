# testmd.md

- Hello
* Hello

# Install and Setup

### 1.Create Database.

Es command ka use DBMS me database create karane ke liye kiya jata hai.
~~~
CREATE DATABASE database_name;
~~~


### 2.Show Databases.

Es command ka use DBMS me jitane bhi database hai onhe dikhan ke liye hota hai.
~~~
SHOW DATABASES;
~~~

### 3. Use Database.

Es command ka use database ko use karane ke liye hota hai.
~~~
USE Database_name;
~~~

### 4. Create Table.

Es command ka use database me table create karane ke liye hota hai.
~~~
CREATE TABLE Table_name (
Column1 DATATYPE CONTRAINT,
Column2 DATATYPE CONTRAINT,
...
);
~~~

### 5.Alter Table.

- #### Add column in table.

Es command ka use table me column add karane ke liye kiya jata hai.
~~~
ALTER TABLE table_name ADD column_name DATATYPE;
~~~

- #### Add column in table specific position.

Es command ka use table me specific column se pahal column add karane ke liye kiya jata hai.
~~~
ALTER TABLE table_name ADD current_column_name AFTER new_cloumn_name;
~~~

- #### Modify column in table.

Es commad ka use table column ko modify karane ke liye kiya jata hai.
~~~
ALTER TABLE table_name MODIFY column_name DATATYPE;
~~~

- #### Rename column in table.

Es command ka use table ke  column ke name ko change karane ke liye kiya jata hai.
~~~
ALTER TABLE table_name RENAME current_column_name TO new_column_name;
~~~

- #### Drop column in table.

Es command ka use table me column ko delete karane ke liye kiya jata hai.
~~~
ALTER TABLE table_name DROP column_name;
~~~
