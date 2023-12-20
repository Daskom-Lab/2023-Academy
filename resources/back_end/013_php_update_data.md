# Update data

How does it feel? Do you still have the enthusiasm? Because now you're gonna edit the data that is existed.

First, you have to make a file named `edit.php`, you can copy the following code:
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Edit Data</title>
</head>
<body>
    <h1>CRUD PHP and MySQL</h1>
    <h2>Edit data</h2>
    <a href="index.php">Show all data</a><br/>
	<h3>Edit data</h3>
    <?php 
	include "connection.php";
	$id = $_GET['id'];
	$query_mysql = mysqli_query($conn, "SELECT * FROM students WHERE id='$id'");
	while($data = mysqli_fetch_array($query_mysql)){
	?>
	<form action="update.php" method="post">		
		<table>
			<tr>
				<td>Name</td>
				<td>
					<input type="text" name="name" value="<?php echo $data['name'] ?>">
				</td>					
			</tr>	
			<tr>
				<td>Student ID</td>
				<td><input type="text" name="student_id" value="<?php echo $data['student_id'] ?>"></td>					
			</tr>	
			<tr>
				<td>Class</td>
				<td><input type="text" name="class" value="<?php echo $data['class'] ?>"></td>					
			</tr>	
			<tr>
				<td></td>
				<td><input type="submit" value="Save"></td>					
			</tr>				
		</table>
	</form>
	<?php } ?>
</body>
</html>
```
The code is pretty same like `input.php`, but there are some default value. The default value is the old value that hasn't been edited. If you want to edit the data, just change the value and save it. But before you do the editing, you have to make a file named `update.php`. You can copy the following code:
```php
<?php 
 
include 'connection.php';
$id = $_POST['id'];
$name = $_POST['name'];
$student_id = $_POST['student_id'];
$class = $_POST['class'];
 
mysql_query("UPDATE students SET name='$name', student_id='$student_id', class='$class' WHERE id='$id'");
 
header("location:index.php?message=update");
?>
```
Just give it a shot and you'll found that the data has been edited.

Keep it going, guys!

GLHF!!!