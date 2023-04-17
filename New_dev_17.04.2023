<html>
    <head>
		<title>Guess US State Capitals</title>
    </head>
    <body>
        <?php
		global $score;
		echo "Currently, your score is: ".$score;
			echo "<pre>\n</pre>";
            $US_Capitals=["Alabama" => "Montgomery", "Alaska" => "Juneau", "Arizona" => "Phoenix", "Arkansas" => "Little Rock", "California" => "Sacramento", "Colorado" => "Denver", "Connecticut" => "Hartford", "Delaware" => "Dover", "Florida" => "Tallahassee", "Georgia" => "Atlanta", "Hawaii" => "Honolulu", "Idaho" => "Boise", "Illinois" => "Springfield", "Indiana" => "Indianapolis", "Iowa" => "Des Moines", "Kansas" => "Topeka", "Kentucky" => "Frankfort", "Louisiana" => "Baton Rouge", "Maine" => "Augusta", "Maryland" => "Annapolis", "Massachusetts" => "Boston", "Michigan" => "Lansing", "Minnesota" => "Saint Paul", "Mississippi" => "Jackson", "Missouri" => "Jefferson City", "Montana" => "Helena", "Nebraska" => "Lincoln", "Nevada" => "Carson City", "New Hampshire" => "Concord", "New Jersey" => "Trenton", "New Mexico" => "Santa Fe", "New York" => "Albany", "North Carolina" => "Raleigh", "North Dakota" => "Bismarck", "Ohio" => "Columbus", "Oklahoma" => "Oklahoma City", "Oregon" => "Salem", "Pennsylvania" => "Harrisburg", "Rhode Island" => "Providence", "South Carolina" => "Columbia", "South Dakota" => "Pierre", "Tennessee" => "Nashville", "Texas" => "Austin", "Utah" => "Salt Lake City", "Vermont" => "Montpelier", "Virginia" => "Richmond", "Washington" => "Olympia", "West Virginia" => "Charleston", "Wisconsin" => "Madison", "Wyoming" => "Cheyenne"];

			//echo "Records loaded: ".count($US_Capitals);	echo "<pre>\n</pre>";
				echo "What is the capital of ";

				$RandomPickOne = array_rand($US_Capitals,4); //choosing 4 random values from $US_Capitals array
				echo($RandomPickOne[0]);
				$right_answ = $RandomPickOne[0]; //assigned first element to its own variable
				// new code 17.04.2023 - store correct answer in a cookie
				$cookie_name = "right_answ";
				$cookie_value = $right_answ;
				setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "/");
				// end of new code 17.04.2023 - store correct answer in a cookie
				
				shuffle($RandomPickOne); // mixing array with 4 randomly selected items

				$option_A = ($US_Capitals[$RandomPickOne[0]]); // assigning
				$option_B = ($US_Capitals[$RandomPickOne[1]]); // mixed elements array
				$option_C = ($US_Capitals[$RandomPickOne[2]]); // to
				$option_D = ($US_Capitals[$RandomPickOne[3]]); // its own variables

        ?>
				<form method="POST"> <!-- action="USSC.php" -->
					A
					<input type="radio" id="option_A" name="SCC_Test_1" value="<?=$option_A?>">
					<label ><?=  $option_A ?></label><br/>
					B
					<input type="radio" id="option_B" name="SCC_Test_1" value="<?=$option_B?>">
					<label ><?=  $option_B ?></label><br/>
					C
					<input type="radio" id="option_C" name="SCC_Test_1" value="<?=$option_C?>">
					<label ><?=  $option_C ?></label><br/>
					D
					<input type="radio" id="option_D" name="SCC_Test_1" value="<?=$option_D?>">
					<label ><?=  $option_D ?></label>
					<br/>
					<input type="submit" name="submit" value="Submit">
					<input type="submit" name="reset" value="Reset">

				</form>

		<?php
		if (isset($_POST['submit'])) {
			if (isset($_POST['SCC_Test_1'])) {
				$SelectedCity = $_POST['SCC_Test_1'];
				echo "<pre>\n</pre>";
				echo "You selected ".$SelectedCity." as the capital of ".$_COOKIE["right_answ"];
				echo "<pre>\n</pre>";
				if ($SelectedCity == ($US_Capitals[$_COOKIE["right_answ"]])) {
						echo "Yum. Thats right!";
/*
						$score = $score +1;
						echo "<pre>\n</pre>";
						echo "Your score is: ".$score;
*/
					} else {
						echo "Nope, not right. The capital of ".$_COOKIE["right_answ"] . " is ";
						echo ($US_Capitals[$_COOKIE["right_answ"]]);
						setcookie("your_score", "", time() - 3600);
					}
				}
			else {
				echo "Nothing detected";
			} 
		}
/*		
		$cookie_name = "your_score";
		$cookie_value = $_COOKIE["your_score"] + $score;
		setcookie($cookie_name, $cookie_value, time() + (86400 * 30), "/");
		echo "<pre>\n</pre>";
		echo "Your score is: ".$_COOKIE["your_score"];
*/
		?>
		<hr>
		<div hidden> <!-- <div hidden> -->
            <?php
            global $count;
            $count = 1;
            echo "<pre>\n</pre>";

            foreach($US_Capitals as $attributes =>$City){
                echo $count." ";
                $count = $count+1;
                echo"$attributes state capital is: $City";
                echo "<pre>\n</pre>";
            }
			?>
		</div>
		<ul>PHP manual and tutorials used:
			<li><a href="https://www.php.net/manual/en/function.array-rand.php">array_rand — Pick one or more random keys out of an array</a></li>
			<li><a href="https://www.php.net/manual/en/function.shuffle.php">shuffle — Shuffle an array</a></li>
			<li><a href="https://www.phptutorial.net/php-tutorial/php-radio-button/">php-radio-button</a></li>
			<li><a href="https://thisinterestsme.com/php-radio-buttons/">php-radio-buttons</a></li>
			<li><a href="https://www.formget.com/php-select-option-and-php-radio-button/">php-select-option-and-php-radio-button</a></li>
			<li><a href="https://stackoverflow.com/questions/31758158/setcookie-fuction-inbetween-head-and-head-or-in-body-section">The setcookie() function must appear BEFORE the &lthtml&gt tag</a></li>
			<li><a href="https://www.php.net/manual/en/language.variables.scope.php">Using $GLOBALS instead of global</a></li>		
		</ul>
		<hr>
    </body?>
</html>
