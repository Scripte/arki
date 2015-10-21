<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>Aliens Abducted Me - Report an Abduction</title>
</head>
<body>
  <h2></h2>

<?php
  $name = $_POST['firstname'] . ' ' . $_POST['lastname'];
  $first_name = $_POST['firstname'];
  $last_name = $_POST['lastname'];
  $email = $_POST['email'];
  
 $dbc = mysqli_connect('localhost' /* или айпи адрес 127.0.0.1 */, 'root', '', 'make_me_elvis' )
 or die ('Error connecting to Mysql server ');
 $query = "INSERT INTO list(first_name,last_name, email ) " .
 "VALUES ('$first_name', '$last_name', ". 
    "  '$email')";
 $result = mysqli_query($dbc, $query)
 or die ('Error quering database ');
 mysqli_close($dbc);
   echo  'custumer added.';

?>
</body>
</html>

