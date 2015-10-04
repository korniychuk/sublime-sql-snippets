MySQL Snippets - Sublime Plugin
==================

A sublime plugin complete with MySQL snippets


**Quick review: http://youtu.be/rQoqbEiFNoU**

Feel free to let me know what else you want added via:

- [Issues](https://github.com/ancor-dev/sublime-sql-snippets/issues)

## What's included - contents
- [Installation](#installation)
- [Database](#database)
- [Table](#table)
- [Table components](#create-table-components)
- [Insert](#insert)
- [Select](#select)
- [Query options](#query-options)
- [Update](#update)
- [Delete](#delete)
- [Alter](#alter---modify-anything)
- [Triggers](#trigger)
- [Procedure](#procedure)
- [Function](#function)
- [Constructions](#constructions)
- [Show](#show)
- [Other](#other)

### Installation

There are 3 methods for installing this plugin.

1. Search for "MySQL Snippets" via the "Package Control: Install Packages" menu.
**Note:** If you don't have Sublime Package Control installed, you can find out how to install it here [https://sublime.wbond.net/installation](https://sublime.wbond.net/installation)

2. Clone the repository into your Sublime Text 2/3 packages directory.
`git clone https://github.com/ancor-dev/sublime-sql-snippets.git`

3. Download the .zip file and unzip it into your Sublime Text 2/3 packages directory.
**Note:** You can find your Sublime Text 2/3 packages directory by going to Preferences > Browse Packages.

### Database
|Snippet Code     | Description    |
|-----------------|----------------|
|s-db             | create a new database |
|s-db-drop        | delete the database |

### Table
|Snippet Code     | Description    |
|-----------------|----------------|
|s-table | create simple table with INT primary key|
|s--table | create simple table with INT primary key, but first remove the old table|
|s-table-tmp| create simple temporary table with engine=memory|
|s--table-tmp| the same, but first remove the old table|

**s-many-many** - Very powerful snippet! Make table for relation *many-to-many*, make two foreign key constrain, and two indexes in it and make two indexes in corresponding tables

### Create Table components
|Snippet Code     | Description    |
|-----------------|----------------|
|s-fk|make foreign key constrain for table creation|
|s--fk|make foreign key constrain for table creation with corresponding indexes|
|s-idx|make default index for table creation|
|s-idx-txt|make FULLTEXT index for table creation|
|s-pk|make primary key|
|s-uk|make unique key|

### Insert
|Snippet Code     | Description    |
|-----------------|----------------|
|s-i|insert multirow|
|s-ione|insert one row|
|s-ifrom|isert data from a sample(other table or database)|

### Select
|Snippet Code     | Description    |
|-----------------|----------------|
|s-s|default *select* for extending with help *query-options*|
|s-sone|*select* one row by *where* condition|
|s-sinline|inline *select* for simple a sample|
|s-smin|inline *select* for search *min* value|
|s-smax|inline *select* for search *max* value|
|s-scount|inline *select* for count rows in the table|


### Query options

**Expressions**

|Snippet Code     | Description    |
|-----------------|----------------|
|s-|the entity. Like `` `table`.`column` ``|
|s--|the entity with a comma. Like ``, `table`.`column` ``|
|s-alias|the entity with alias. Like `` `table`.`column` AS `my_col` ``|
|s--alias|the same with comma. Like ``, `table`.`column` AS `my_col` ``|
|s-and| a part of conditions `` AND ( ... ) `` |
|s-or| a part of conditions `` OR ( ... ) `` |
|s--and| a part of conditions with expression `` AND ( `col` = `col2` ) `` |
|s--or| a part of conditions with expression `` OR ( `col` = `col2` ) `` |
|s-e| an expression ``( `col` = `col2` )``|


**Statements**

|Snippet Code     | Description    |
|-----------------|----------------|
|s-f|`from` statement like `` FROM `table` AS `alias` ``|
|s-j|`inner join` statement|
|s-jleft|`left join` statement|
|s-jright|`right join` statement|
|s-w|`where` statement|
|s-o|`order by` statement|
|s-l|`limi` statement|
|s-g|`group by` statement|
|s-h|`having` statement|
|s-u|`union` statement|


### Update
|Snippet Code     | Description    |
|-----------------|----------------|
|s-u|default `update` snippet with `where` condition|

### Delete
|Snippet Code     | Description    |
|-----------------|----------------|
|s-d|default `delete` snippet with `where` condition|

### Alter - modify structure
All `alter` snippets begining from ``s-alter-*`` prefix, like `s-alter-add`.

**Columns**

|Snippet Code     | Description    |
|-----------------|----------------|
|add|add a column to table at the last column|
|add-first|add a column to table at the first column|
|add-after|add a column to table after someone column|
|auto-increment|change `auto_increment` counter value|
|change|`change` the column(rename or change type)|
|modify|`modify` the column(change type and column order)|
|drop|drop the column from the table|

**Other**

|Snippet Code     | Description    |
|-----------------|----------------|
|index|add an index to the table|
|index-drop|drop the index from the table|
|order|sort the table by column(yes it indeed possible!)|
|table-rename|rename the table|
|table-charset|change table charset and collate|
|db-charset|change database charset and collate|
|fk|add foreign key to the table|
|-fk|add foreign key to the table with index|
|fk-drop|drop the foreign key from the table|


### Trigger

|Snippet Code     | Description    |
|-----------------|----------------|
|s-trigger|create new trigger|
|s-trigger-drop|drop the trigger|

### Procedure

|Snippet Code     | Description    |
|-----------------|----------------|
|s-proc|create new storage procedure|
|s-proc-drop|drop the storage procedure|
|s-proc-list|show procedures list(only current database)|

### Function

|Snippet Code     | Description    |
|-----------------|----------------|
|s-func|create new function|
|s-func-drop|drop the function|
|s-func-list|show functions list(only current database)|

### Show
|s-hcols|details of the table (*SHOW FULL COLUMNS FROM ...*)|
|s-hcreate|show command for creating the table (*SHOW CREATE TABLE ...*)|
|s-hidx|show indexes for the table (*SHOW INDEX FROM ...*)|

### Constructions

|Snippet Code     | Description    |
|-----------------|----------------|
|s-if|create `if`  statement|
|s--if|create `if else` statement|

### Other

|Snippet Code     | Description    |
|-----------------|----------------|
|s-delim|make `delimiter $$` statement and at the end `delimiter ;`
|s-utc|select current `timestamp`|