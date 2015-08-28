MySQL Snippets - Sublime Plugin
==================

A sublime plugin complete with MySQL snippets

Feel free to let me know what else you want added via:

- [Issues](https://github.com/ancor-dev/sublime-sql-snippets/issues)

## What's included - contents
- [Database](#database)
- [Table](#table)

### Database
|Snippet Code     | Description    |
|:---------------:|----------------|
|s-db             | create a new database |
|s-db-drop        | delete the database |

### Table
|Snippet Code     | Description    |
|:---------------:|----------------|
|s-table | create simple table with INT primary key|
|s--table | create simple table with INT primary key, but first remove the old table|
|s-table-tmp| create simple temporary table with engine=memory|
|s--table-tmp| the same, but first remove the old table|
|s-desc|details of the table(*SHOW FULL COLUMNS FROM*)|
|**s-many-many**| Very powerful snippet! Make table for relation *many-to-many*, make two foreign key constrain, and two indexes in it and make two indexes in corresponding tables|

**Create Table components**
|Snippet Code     | Description    |
|:---------------:|----------------|
|s-fk|make foreign key constrain for table creation|
|s-ids|make default index for table creation|
|s-ids-txt|make FULLTEXT index for table creation|
