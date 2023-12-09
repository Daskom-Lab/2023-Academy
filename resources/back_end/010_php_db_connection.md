# DB Connection

PHP is a server-side scripting language, which should be able to be connected to database. So before doing some CRUD, you have to make a connection to the database. Before you do the connection, you should have at least one database (maybe you do have if you did hands-on in the previous section), if you have a database, let's get move on.

First, you should create a folder (name it whatever you want) in the htdocs folder (if you use XAMPP) or www (if you use Laragon). 

Now, create `connection.php` in the folder and type the following syntax:
```php
<?php

$conn = mysqli_connect("localhost", "root", "", "schoolDB");

?>
```

<strong>What does that mean?</strong>
<br>
`mysqli` is on of a driver in PHP that make us able to make a database connection. We can use `mysqli_connect()` syntax to connect to the database we want. `localhost` is a host name, in production you can use IP address. `root` is your MySQL username. It was specified automatically the time you download MySQL. There's no default password, so after `root`, there's just `""` for password argument. `schoolDB` is the name of the database you want to be connected to your php code.

Save the code, and you know what? You've done making database connection :)

After that, so what? We can go to the next section, we'll create a simple CRUD application. See you there!

GLHF!