

<!DOCTYPE html>
<html lang="en">
	
	
		<head>
			<title> Order Page </title>
			<link rel="stylesheet" href="css/style.css" type="text/css">
			<link href="https://fonts.googleapis.com/css2?family=Akaya+Telivigala&display=swap" rel="stylesheet">
		</head>
	
		<body>
			<ul class="menu">
		  	<li><a href="index.html">Home</a> </li>
			 	<li><a href="about.html">About</a> </li>
				<li><a href="contact.html">Contact</a> </li>
				<li><a class="active" href="order.html">Order</a> </li>
		  </ul>
			
			<h1 class="head">Order from NoGutsNoGlory Pizzeria</h1>
			<br>
			
			<p class="category">Toppings:</p>
			<br>
			<form class="order" method="post" action="https://www.stonecoldprofessor.com/pizza-order.php">
			<p class="contact">Meats</p>
			<input type="checkbox" name="toppings[]" value="bacon">Bacon
			<input type="checkbox" name="toppings[]" value="bbq chicken">BBQ Chicken
			<input type="checkbox" name="toppings[]" value="chorizo">Chorizo
			<input type="checkbox" name="toppings[]" value="ham">Ham
			<input type="checkbox" name="toppings[]" value="meatballs">Meatballs
			<input type="checkbox" name="toppings[]" value="pepperoni">Pepperoni
			<input type="checkbox" name="toppings[]" value="salami">Salami
			<input type="checkbox" name="toppings[]" value="sausage">Sausage
			<br>
			<br>
			<p class="contact">Vegetables</p>
			<input type="checkbox" name="toppings[]" value="mushroom">Mushrooms
			<input type="checkbox" name="toppings[]" value="olive">Olives
			<input type="checkbox" name="toppings[]" value="onion">Onions
			<input type="checkbox" name="toppings[]" value="green peppers">Green Peppers
			<input type="checkbox" name="toppings[]" value="spinach">Spinach
			<input type="checkbox" name="toppings[]" value="artichoke heart">Artichoke Hearts
			<input type="checkbox" name="toppings[]" value="red peppers">Red Peppers
			<input type="checkbox" name="toppings[]" value="scallion">Scallions
			<input type="checkbox" name="toppings[]" value="red onion">Red Onions
			<br>
			<br>
			<p class="contact">Cheese</p>
			<input type="checkbox" name="toppings[]" value="extra cheese">Extra Cheese
			<input type="checkbox" name="toppings[]" value="blue cheese">Blue Cheese
			<input type="checkbox" name="toppings[]" value="feta">Feta
			<input type="checkbox" name="toppings[]" value="colby">Colby
			<input type="checkbox" name="toppings[]" value="cheddar">Cheddar
			<input type="checkbox" name="toppings[]" value="parmesan">Parmesan
			<input type="checkbox" name="toppings[]" value="mozzarella">Mozzarella
			<input type="checkbox" name="toppings[]" value="romano">Romano
			<br>
			<br>
			<p class="contact">Other</p>
			<input type="checkbox" name="toppings[]" value="basil">Basil
			<input type="checkbox" name="toppings[]" value="chivs">Chives
			<input type="checkbox" name="toppings[]" value="garlic">Garlic
			<input type="checkbox" name="toppings[]" value="cilantro">Cilantro
			<input type="checkbox" name="toppings[]" value="jalapeno">Jalapenos
			<input type="checkbox" name="toppings[]" value="oregano">Oregano
			<input type="checkbox" name="toppings[]" value="parley">Parley
			<input type="checkbox" name="toppings[]" value="pepper">Pepper		
			<input type="checkbox" name="toppings[]" value="anchovies">Anchovies
			<input type="checkbox" name="toppings[]" value="shrimp">Shrimp
			<input type="checkbox" name="toppings[]" value="salmon">Salmon
			<input type="checkbox" name="toppings[]" value="oysters">Oysters
			<br>
			
			<br>
			<p class="category">Crust Style:</p>
			<br>
      <input name="crust" value="thin" type="radio">Thin
      <input name="crust" value="thick" type="radio">Thick
      <input name="crust" value="pan" type="radio">Pan
      <input name="crust" value="chicago style" type="radio">Chicago
			<input name="crust" value="flat bread" type="radio">Flat Bread
			<input name="crust" value="deep dish" type="radio">Deep Dish
			<input name="crust" value="silican" type="radio">Silican
			<input name="crust" value="focacia" type="radio">Focaccia
			<input name="crust" value="new york-style" type="radio">New York-Style
			<br>
			
			<br>
			<p class="category">Size of pizza:</p>
			<br>
			<select name="size">
			<option value="Small">Small</option>
			<option value="Medium">Medium</option>
			<option value="Large">Large</option>
			<option value="Extra Large"> XTRA Large</option>
			</select>
			<br>
			
			<br>
			<p class="contact">Enter Information below</p>
			<input name="first" placeholder="First Name" type="text" required><br>
			<input name="last" placeholder="Last Name" type="text" required><br>
			<input name="add1" placeholder="Address Line" type="text" required><br>
			<input name="add2" placeholder="Address Line 2" type="text"><br>
			<input name="city" placeholder="City" type="text" required><br>
			
			<select name="state">
			<option value="State">State</option>
			<option value="Alabama">AL</option>
			<option value="Alaska">AK</option>
			<option value="Arizona">AZ</option>
			<option value="Arkansas">AR</option>
			<option value="California">CA</option>
			<option value="Colorado">CO</option>
			<option value="Connecticut">CT</option>
			<option value="Delaware">DE</option>
			<option value="Florida">FL</option>
			<option value="Georgia">GA</option>
			<option value="Hawaii">HI</option>
			<option value="Idaho">ID</option>
			<option value="Illinois">IL</option>
			<option value="Indiana">IN</option>
			<option value="Iowa">IA</option>
			<option value="Kansas">KS</option>
			<option value="Kentucky">KY</option>
			<option value="Louisiana">LA</option>
			<option value="Maine">ME</option>
			<option value="Maryland">MD</option>
			<option value="Massachusetts">MA</option>
			<option value="Michigan">MI</option>
			<option value="Minnesota">MN</option>
			<option value="Mississippi">MS</option>
			<option value="Missouri">MO</option>
			<option value="Montana">MT</option>
			<option value="Nebraska">NE</option>
			<option value="Nevada">NV</option>
			<option value="New Hampshire">NH</option>
			<option value="New Jersey">NJ</option>
			<option value="New Mexico">NM</option>
			<option value="New York">NY</option>
			<option value="North Carolina">NC</option>
			<option value="North Dakota">ND</option>
			<option value="Ohio">OH</option>
			<option value="Oklahoma">OK</option>
			<option value="Oregon">OR</option>
			<option value="Pennsylvania">PA</option>
			<option value="Rhode Island">RI</option>
			<option value="South Carolina">SC</option>
			<option value="South Dakota">SD</option>
			<option value="Tennessee">TN</option>
			<option value="Texas">TX</option>
			<option value="Utah">UT</option>
			<option value="Vermont">VT</option>
			<option value="Virginia">VA</option>
			<option value="Washington">WA</option>
			<option value="West Virginia">WV</option>
			<option value="Wisonsin">WI</option>
			<option value="Wyoming">WY</option>
			</select>
			<br>
			
			<input name="zip" placeholder="Zip" type="text" required><br>
			<input name="phone" placeholder="Phone Number" type="text" required><br>
			<input name="email" placeholder="Email Address" type="text" required><br>
			
			<textarea name="comments" placeholder="Comments"></textarea><br>	
	
			<input type="reset">
			<input type="submit">
			</form>
			
		</body>
			
</html>
