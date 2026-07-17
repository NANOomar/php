# php
<?php
echo "<h1>Welcome to My Website</h1>";
echo "<p>Apache + PHP + PostgreSQL is working!</p>";

																																										//varibels 
        $name = "Nano Omar";
        $food = "pizza";
        $age = 19;
        $users = 3;
        $quantity = 3;
        $gpa = 2.5;
        $price = 4.99;
        $employed = true;
        $online = false;

        //echo $name;
        echo "Hello {$name}<br>";
        echo "You like {$food}<br>";
        echo "you are {$age} years old<br>";
        echo "There  are {$users} users online <br>";
        echo "You would like to buy {$quantity} items<br>";
        echo "Your gpa is {$gpa}<br>";
        echo "your pizza is \${$price}<br>";
        $total = null;
        echo "you have ordered {$quantity} x {$food}<br>";
        $total = $price * $quantity;
        echo "you total order is \${$total}";


?>


<?php
    //arithmetic operators 
    //+- */ ** %

    $x = 10;
    $y = 2;
    $z = null;

    //$z = $x + $y;
    //$z = $x - $y;
    //$z = $x * $y;
    //$z = $x / $y;
    //$z = $x ** $y; //-> power
    $z = $x % $y;
    //echo $z;

    //Incrementing / Decrementing ++ --;
    $counter = 0;

    $counter++;
    $counter--;
    $counter+=2;
    $counter-=2;
    echo $counter;


    //Operator Precedence
    //() ** * / % + -

?>
																																			//$_GET
																																			//$_POST
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>Username : </label>
        <input type="text" name="username"><br>
        <label>Password : </label>
        <input type="password" name="password"><br>
        <input type="submit" value="login">
    </form>
</body>
</html>
																								
<?php
																												//$_GET =  Data is appended to the url
																											//         NOT SECURE
																											//         char limit
																											//         Bookmark is possible w/ values
																											//         GET requests can be cached
																											//         Better for a search page


																											//$_POST = Data is packaged inside the body of the HTTP request
																											//         MORE SECURE
																											//         No data limit
																											//         Cannot bookmark
																											//         requests are not cached
																											//         Better for submitting credentials
    echo $_POST["username"] . "<br>";
    echo $_POST["password"] . "<br>";
?>




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>Quantity : </label>
        <input type="text" name="quantity">
        <input type="submit" value="total">
    </form>
</body>
</html>

<?php
    $item = "pizza";
    $price = 3.99;
    $quantity = $_POST["quantity"];
    $total = null;
    echo "you ordered {$quantity} {$item}";
    $total = $quantity * $price;
    echo "the total is : {$total}";
?>


																																			//math function 


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>x : </label>
        <input type="text" name="x"><br>
        <label>y : </label>
        <input type="text" name="y"><br>
        <label>z : </label>
        <input type="text" name="z"><br>
        <input type="submit" value="result">
    </form>
</body>
</html>

<?php
    $x = $_POST["x"];
    $y = $_POST["y"];
    $z = $_POST["z"];
    $total = null;

    //$total = abs($x);
    //$total = round($x); //3.44 > 3 ,, 3.99 > 4
    //$total = floor($x);
    //$total = ceil($x);

    //$total = pow($x , $y);
    //$total = sqrt($x);
    //$total = max($x , $y , $z);
    //$total = min($x , $y , $z);
    //$total = pi();
    //$total = rand();
    $total = rand(1 , 6);

    echo $total;
?>



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>enter the reduis : </label><br>
        <input type="text" name="raduis"><br>
        <input type="submit" value="calculate">

    </form>
</body>
</html>

<?php
    $r = $_POST["raduis"];

    $circunference = 2 * pi() * $r;
    $circunference = round($circunference , 2);
    
    $area = pi() * $r;
    $area = round($area , 2);

    $volume = 4 / 3 * pi() * pow($r , 3);
    $volume = round($volume , 2);

    echo $circunference . "<br>";
    echo $area . "<br>";
    echo $volume . "<br>";

?>



																																						//if elseif else
<?php
    //if(condition){
    //}
    //elseif(condition){
    //}
    //else{
    //}
?>
																																					//&& || !
																																					
																																					
																																				//switch(){	}
<?php
  $grade = "v";

  switch($grade){
    case "A":
        echo "You did great";
        break;
    case "B":
        echo "you did good";
        break;
    case "C":
        echo "you did okey";
        break;
    case "D":
        echo "you did properly";
        break;
    case "F":
        echo "you Failed";
        break;
    default:
        echo "The grade \"{$grade}\" is not vadid";
  }

?>


<?php


    $date = date("l");
    
    switch($date){
        case "Monday":
            echo "I hate Mondays";
            break;
        case "Teusday":
            echo "tacco tusday";
            break;
        case "Wednsday":
            echo "biig boobs are the perfect choice";
            break;
        case "thersday":
            echo "IDK";
            break;
        case "Friday":
            echo "friday wiiw";
            break;
        case "Saturday":
            echo "work home day";
            break;
        case "Sunday":
            echo "niggaaaa";
            break;
        default:
            echo "wtf is this day";
    }
?>

																																				
																																				
																																			//for loop	

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>Enter a number to count to :</label><br>
        <input type="text" name="num">
        <input type="submit" , value="count">
        
    </form>
</body>
</html>

<?php
    $num = $_POST["num"];

    for($i = 0 ; $i <= $num ; $i++){
        echo "{$i}<br>";
    }
?>




																																			//while loop
																																			//isset(button) //clicked


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <input type="submit" value="stop" name="stop">
    </form>
</body>
</html>
    

<?php
    $isRunning = true;
    $counter = 0;

    while($isRunning){
        if(isset($_POST["stop"])){
            $isRunning = false;
        }

        echo "{$counter} <br>";
        $counter++;
    }
?>


																											//ssion



<?php
    $foods = array("orange" , "banana" , "coconut" , "apple");

    //$foods[0] = "pineapple";
    //array_push($foods , "pineaple" , "kiwi");
    //array_pop($foods);
    //array_shift($foods);
    //$reversed_foods = array_reverse($foods);
    //echo count($foods);
    foreach($foods as $food){
        echo "{$food} <br>";
    }
?>


																																			//acociative array = key -> value
																																			
																																			
																																			
																																			
																																			
																																			
																																			
																																			
<?php
    $capitals = array("USA" => "washington D.C" , 
                      "Morocco" => "Rabat" ,
                      "Japan" => "Tokyo" ,
                      "South Korea" => "Seoul");

    //$capitals["USA"] = "NANO";
    //$capitals["China"] = "Benjing";
    //array_pop($capitals);
    //array_shift($capitals);
    //$keys = array_keys($capitals);
    //$values = array_values($capitals);
    //$capitals = array_flip($capitals);
    //$capitals = array_reverse($capitals);



    //foreach($capitals as $capital){
    //    echo "{$capital} <br>";
    //}

    foreach($capitals as $key => $value){
        echo " {$key} = {$value} <br>";
    }

    //foreach($values as $value){
    //    echo " {$value} <br>";
    //}
?>







<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>Enter your country</label>
        <input type="text" name="country">
        <input type="submit">
    </form>
</body>
</html>
    

<?php
    $capitals = array("USA" => "washington D.C" , 
                      "Morocco" => "Rabat" ,
                      "Japan" => "Tokyo" ,
                      "South Korea" => "Seoul");


    $country = $_POST["country"];
    foreach($capitals as $key => $value){
        if($key == $country){
        echo "{$value}";
        }
    }

    //$capital = $capitals[$_POST["country"]];
?>



																																				//isset() = retrun true if the varible is declared and and not null
																																				//empty() = return true if the varible is not declared , false , null , ""
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <label>Username : </label>
        <input type="text" name="username"><br>
        <label>password</label>
        <input type="password" name="password"><br>
        <input type="submit" name="submit" value="log in">
    </form>
</body>
</html>
    

<?php
    
    $submit = $_POST["submit"];

    if(isset($submit)){

        $username = $_POST["username"];
        $password = $_POST["password"];

        if(empty($username)){
            echo "Username is missing";
        }
        elseif(empty($password)){
            echo "password is missing";
        }
        else{
            echo "Hello {$username}";
        }
    }
?>


																																					//radio

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <input type="radio" name="credit_card" value="Visa">
        visa<br>
        <input type="radio" name="credit_card" value="MasterCard">
        MasterCard<br>
        <input type="radio" name="credit_card" value="AmericanExpress">
        American Express<br>
        <input type="submit" name="confirm" value="confirm">
    </form>
</body>
</html>
    

<?php

    if(isset($_POST["confirm"])){

        if(isset($_POST["credit_card"])){
            $credit_card = $_POST["credit_card"];
        }

        if($credit_card == "Visa"){
            echo "You selected Visa";
        }
        elseif($credit_card == "MasterCard"){
            echo "You selected MasterCard";
        }
        elseif($credit_card == "AmericanExpress"){
            echo "You selected American Express";
        }
        else{
            echo "please make a selection ";
        }
        
    }
?>


																																							//check box
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <input type="checkbox" name="pizza" value="Pizza">Pizza<br>
        <input type="checkbox" name="hamberger" value="Hamberger">Hamberger<br>
        <input type="checkbox" name="hotdog" value="Hotdog">Hotdog<br>
        <input type="checkbox" name="taco" value="Taco">Taco<br>
        <input type="submit" name="submit">

    </form>
</body>
</html>
    

<?php
    //beter use empty()
    if(isset($_POST["submit"])){

        if(isset($_POST["pizza"])){
            echo "You like pizza<br>";
        }
        else{
            echo "You DON'T like pizza<br>";
        }
        if(isset($_POST["hamberger"])){
            echo "You like hamberger<br>";
        }
        else{
            echo "You DON'T like hamberger<br>";
        }
        if(isset($_POST["hotdog"])){
            echo "You like hotdog<br>";
        }
        else{
            echo "You DON'T like hotdog<br>";
        }
        if(isset($_POST["taco"])){
            echo "You like taco<br>";
        }
        else{
            echo "You DON'T like taco<br>";
        }
    }

?>




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.php" method="post">
        <input type="checkbox" name="foods[]" value="Pizza">Pizza<br>
        <input type="checkbox" name="foods[]" value="Hamberger">Hamberger<br>
        <input type="checkbox" name="foods[]" value="Hotdog">Hotdog<br>
        <input type="checkbox" name="foods[]" value="Taco">Taco<br>
        <input type="submit" name="submit">

    </form>
</body>
</html>
    
    
<?php
    if(isset($_POST["submit"])){
        $foods = $_POST["foods"];

        foreach($foods as $food){
            echo "{$food}<br>";
        }
    }
?>



																																					//function

    
<?php
    function happyBirthday($firstname , $age){
        echo "happy birthday {$firstname}<br>";
        echo "happy birthday to you!<br>";
        echo "you are now {$age}<br><br>";
    }
    

    happyBirthday("nano" , 19);
    happyBirthday("omar" , 29);



    function hypotenuse(float $a , float $b){
        $c = sqrt($a ** 2 + $b ** 2);
        return $c;
    }
?>



																																		//string functions
    
<?php
    $username = "Nano omar";
    $phon_num = "1234-5678-9000";

    $username = strtolower($username);
    $username = strtoupper($username);
    $username = trim($username); //"      bbb       "
    $username = strtolower($username);
    $username = str_pad($username , 20 , 0); //-> "Nano omar00000000000"
    $phon_num = str_replace("-" , "" , $phon_num);
    $username = str_shuffle($username);
    $eqaul = strcmp($username , "nano omar"); //> 0 == ; -1/1
    $username = strlen($username);
    $index = strpos($username ," ");
    $firsname = str_pad($username , 0 , 4);
    $lastname = str_pad($username , 5);
    $fillname = explode(" " , $username); //< new array

    $username2 = array("Nano", "the", "negatron" ,"omar");
    $lastname = implode("-" , $username2);//>"Nano-the-negatron-omar"

?>














<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="index.html" method="post">
        username:<br>
        <input type="text" name="username"><br>
        age:<br>
        <input type="text" name="age"><br>
        <input type="submit" name="submit" value="log in">
    </form>
</body>
</html>
    
<?php
    
    if(isset($_POST["submit"])){
        $username = filter_input(INPUT_POST , "username" , 
                                FILTER_SANITIZE_SPECIAL_CHARS);
        $age = filter_input(INPUT_POST , "age" ,
                            FILTER_SANITIZE_NUMBER_INT);

        echo "you are {$age} years old";
    }
?>

																																																//validate user input 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

<form action="index1.php" method="post">
    username:<br>
    <input type="text" name="username"><br>

    age:<br>
    <input type="text" name="age"><br>

    email:<br>
    <input type="text" name="email"><br>

    <input type="submit" name="submit" value="log in">
</form>

</body>
</html>

<?php

if (isset($_POST["submit"])) {
    $username = filter_input(INPUT_POST, "username",
        FILTER_SANITIZE_SPECIAL_CHARS);

    $age = filter_input(INPUT_POST, "age",
        FILTER_SANITIZE_NUMBER_INT);

    $email = filter_input(INPUT_POST, "email",
        FILTER_SANITIZE_EMAIL);

    echo "you are {$email} years old";
}

?>




<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

<form action="index1.php" method="post">
    username:<br>
    <input type="text" name="username"><br>

    age:<br>
    <input type="text" name="age"><br>

    email:<br>
    <input type="text" name="email"><br>

    <input type="submit" name="submit" value="log in">
</form>

</body>
</html>

<?php

if (isset($_POST["submit"])) {
    $username = filter_input(INPUT_POST, "username",
        FILTER_SANITIZE_SPECIAL_CHARS);

    $age = filter_input(INPUT_POST, "age",
        FILTER_VALIDATE_INT);

    $email = filter_input(INPUT_POST, "email",
        FILTER_VALIDATE_EMAIL);

    if(empty($age)){
        echo "this age is not valid";
    }
    else{
        echo "your age is {$age}";
    }

    if(empty($email)){
        echo "this email is not valid";
    }
    else{
        echo "your email is {$age}";
    }
}

?>




//index.php
<?php
    include("header.html");
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>this is the HOME page</p>
    <p>Stuff about the home page</p>
</body>
</html>


<?php
    include("footer.html");
?>

//about.php
<?php
    include("header.html");
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>this is the About page</p>
    <p>Stuff about the ABOUT page</p>
</body>
</html>


<?php
    include("footer.html");
?>

//location.php
<?php
    include("header.html");
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>this is the LOCATIONS page</p>
    <p>Stuff about the LOCATION page</p>
</body>
</html>


<?php
    include("footer.html");
?>

//header.html
<header>
    <h1>This is Nano omar website</h1><br>
    <a href="index1.php">Home</a>
    <a href="location.php">Location</a>
    <a href="about.php">About</a>
    <hr>
</header>



//footer.html
<footer>
    <hr>
    <b>Author: Nano Omar</b><br>
    <a href="0Omar.el.ghazali@gmail.com">0Omar.el.ghazali@gmail.com</a>
</footer>


																																				// cookie = Information about a user stored in a user's web-browser
																																				//          targeted advertisements, browsing preferences, and
																																				//          other non-sensitive data
																																				//         inspect aplication cookies


<?php

setcookie("fav_food" , "pizza" , time() + 0 , "/");
setcookie("fav_drink" , "coffe" , time() + (86400 * 3) , "/");
setcookie("fav_dessert" , "ice cream" , time() + (86400 * 4) , "/");


foreach($_COOKIE as $key => $value){
    echo "{$key} = {$value}<br>";
}

if(isset($_COOKIE["fav_food"])){
    echo "buy some {$_COOKIE["fav_food"]} !!!";
}
else{
    echo "I don't know what is your favorite food!";
}
?>




																																														//session

//index.php
<?php
    session_start();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>this is the login page</h2>
    <a href="home.php">this is goes to login page</a>
</body>
</html>

<?php
    $_SESSION["username"] = "nanoomar";
    $_SESSION["password"] = "nanoomar";

    echo "<br>{$_SESSION["username"]}<br>";
    echo "{$_SESSION["password"]}<br>"

?>

//home.php
<?php
    session_start();
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h2>this is the home page</h2>
    <a href="index1.php">this is goes to login page</a>
</body>
</html>


<?php
    echo "<br>{$_SESSION["username"]}<br>";
    echo "{$_SESSION["password"]}<br>"

?>




																																														//htmlspecialchars($_SERVER["PHP_SELF"]) -> to get the name of the curent file
																																														
																																														//$_server

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="<?php htmlspecialchars($_SERVER["PHP_SELF"])?>" method="post">
        <h2>this is the login page</h2>
        username:<br>
        <input type="text" name="username"><br>
        <input type="submit" name="login" value="login" >

    </form>
    
</body>
</html>

<?php
    /*if(isset($_POST["submit"])){
        //code
    }*/


    if($_SERVER["REQUEST_METHOD"] == "POST"){
        echo "hello";
    }
?>

																																																						//password hashing
<?php
    $password = "nanoomar";

    $hash = password_hash($password , PASSWORD_DEFAULT);

    if(password_verify("ninoomar" , $hash)){
        echo "you are loged in!";
    }
    else{
        echo "password incorrect";
    }
?>










																																										//inser into mysql 


<?php
    include("database.php");

    $username = "nano";
    $password = "aloalo"; 
    $hash = password_hash($password , PASSWORD_DEFAULT);

    $sql = "INSERT INTO users (user, password)
            VALUES ('$username' , '$hash')";

    try{
        mysqli_query($conn, $sql);
        echo "user register seccess";
    }
    catch(mysqli_sql_exception){
        echo "could not register this user!";
    }
    
    mysqli_close($conn);
?>



																																										//query database
													//one user
<?php 
    include("database.php");


    $sql = "SELECT * FROM users WHERE user = 'nano'";
    $result = mysqli_query($conn , $sql);

    if(mysqli_num_rows($result) > 0){
        $row = mysqli_fetch_assoc($result);
        echo $row["id"] . "<br>";
        echo $row["user"] . "<br>";
        echo $row["password"] . "<br>";
        echo $row["reg_date"] . "<br>";
    }
    else{
        echo "user not found";
    }
    mysqli_close($conn);

?>
																													//many users 
<?php 
    include("database.php");


    $sql = "SELECT * FROM users";
    $result = mysqli_query($conn , $sql);

    if(mysqli_num_rows($result) > 0){
        while($row = mysqli_fetch_assoc($result)){
            echo $row["id"] . "<br>";
            echo $row["user"] . "<br>";
            echo $row["password"] . "<br>";
            echo $row["reg_date"] . "<br>";
        }
        
    }
    else{
        echo "user not found";
    }
    mysqli_close($conn);

?>




																																																//last vid


<?php 
    include("database.php")
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <form action="<?php htmlspecialchars($_SERVER["PHP_SELF"])?>" method="post">
        <label>username</label><br>
        <input type="text" name="username"><br>
        <label>password</label><br>
        <input type="password" name="password"><br>
        <input type="submit" value="register" name="register"><br>
    </form>
</body>
</html>

<?php 
    if($_SERVER["REQUEST_METHOD"] == "POST"){
        
        $username = filter_input(INPUT_POST , "username" , FILTER_SANITIZE_SPECIAL_CHARS);
        $password = filter_input(INPUT_POST , "password" , FILTER_SANITIZE_SPECIAL_CHARS);

        if(empty($username)){
            echo "username is messing";
        }
        elseif(empty($password)){
            echo "password is messing";
        }
        else{
            $hash = password_hash($password , PASSWORD_DEFAULT);

            $sql = "INSERT INTO users (user_name , password)
                                 VALUES('$username' , '$hash')";
                                 echo "{$username} = {$password}";
            try{
                mysqli_query($conn , $sql);
                echo "username registered seccesfully";
            }
            catch(mysqli_sql_exception){
                echo "could not register this user!!";
                echo "this username is taken!";

            }
        }
    }

    mysqli_close($conn);
?>
