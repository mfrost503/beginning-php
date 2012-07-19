#Level 3 PDO Tutorial#
With the impending removal the of MySQL extension for PHP, it's important to understand how to use the alternatives.
PDO is the most flexible option because it allows to integrate with multiple database engines just by changing the
Data Source Name.

An important note, PDO ships with PHP 5.1 and up and is available as PECL extension for PHP 5.0.  It is not availble,
in PHP 4.x, make sure you upgrade from 4 if you'd like to utilize this tool

##Connecting
Before you can get any information into and/or out of a database, you have to know how to connect.  With PDO, you
instantiate a new PDO object and provide a Data Source Name or DSN.
```
$dsn = "mysql:host=localhost;dbname=tutorial";
$user = 'tut_example';
$pass = 'pass123';
$dbh = new PDO($dsn,$user,$pass);
 ```
The example above is connecting to a MySQL data source, to use a different engine like Postgres the DSN can be 
constructed a little differently.
```
$dsn = "pgsql:host=localhost;dbname=tutorial;user=tut_example;password=pass123";
$dbh = new PDO($dsn);
```


