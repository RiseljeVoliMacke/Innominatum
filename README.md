function jsdebug($tmp)
{
	echo "<script>console.log(\"".$tmp."\")</script>";
}

function openConn()
{
	global $conn, $index;
	$user = "root";
	$pass = "";
	$dbname = "";

	$conn = new mysqli("localhost", $user, $pass, $dbname);
	if ($conn->connect_error) 
		die("Connection failed: " . $conn->connect_error);
	
}

<div class="container">
	<div class="dummy"></div>
	<div class="loader"></div>
	<p id="redirection_timer"></p>
</div>

<script> redirect(); </script>

echo "<p class=\"succes\">Oglas uspješno obrisan</p>";
die("<p class=\"permError\">Oglas nije mogao biti obrisan</p>");