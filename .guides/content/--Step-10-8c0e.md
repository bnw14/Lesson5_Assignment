<h1>Step 10 - Add the home/away information to the calendar using <code>if</code> statements</h1>

<ol>
<li>Return to the <b>seminole.js</b> file.</li>

<<<<<<< HEAD
<<<<<<< HEAD
<li>Within the <code>addGameInfo()</code> function, within the data block for the for loop, insert a new line before the final statement in the for-loop, enter the code <b>if (gameLocation[i] === "away")  {, </b>press <b>ENTER</b> twice, and then enter a closing <b>}</b> as shown below:

<pre>
=======
=======
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
<li>Within the <code>addGameInfo()</code> function, within the data block for the for loop, insert a new line before the final statement, enter the code <b>if (gameLocation[i] === "away")  {, </b>press <b>ENTER</b> twice, and then enter a closing <b>}</b> as shown below:

<pre>
paragraphs = tableCell.getElementsByTagName("p");

<<<<<<< HEAD
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
=======
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
<mark>if (gameLocation[i] === "away") {  </mark>


<mark>}//end of if</mark> </pre>
This code starts with <code>if</code> statement, followed by parentheses containing the <code>if</code> condition.  The statement tests whether the element of the <code>gameLocation</code> array with the index value equal to the counter variable, i, equals the string "away".
</li>



<li>Within the block for the <code>if</code> statement, enter the statement <b>paragraphs[i].innerHTML = "@ ";</b> as shown below:
<pre>
if (gameLocation[i] === "away") {
<<<<<<< HEAD
<<<<<<< HEAD
    <mark>paragraphs[1].innerHTML = "@ ";</mark>
    <mark>paragraphs[1].innerHTML += opponents[i];</mark>
}//end of if</pre>
This statement sets the content of the first paragraph in the current cell equal to "@".
</li>

=======
=======
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
<mark>paragraphs[1].innerHTML = "@ ";</mark>
}</pre>
This statement sets the content of the first paragraph in the current cell equal to "@".
</li>


<li>
Below the block you just created, in the final block of code for the <code>for</code> loop change = to += so that the statement matches the following:
<pre>
paragraphs[1].innerHTML <mark>+=</mark> opponents[i];
</pre>

Because you've just added content to the second paragraph using your <code>if</code> statement, you want to ensure that the name of the opposing team is concatenated to the existing content (+=) rather than replacing it (=).
</li>



<<<<<<< HEAD
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
=======
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
<li>Reload the <b>calender.htm</b> and view the web page.  As you can see, <b>"@"</b> followed by a space is now displayed before the opponent names in some of the table cells.  These dates correspond to the elements in the <code>gameLocation</code> array with a value of "away". </li>


<center><img src=".guides/img/SeminoleTrojan_Away.png" alt="Seminole Trojans" /></center>

<li>
In order to add the text "vs" followed by a space before the names of the opponents for home games, you need to create another <code>if</code> statement.
<br>
<<<<<<< HEAD
<<<<<<< HEAD
Immediately after the closing <code>}</code> for the <code>if</code> statement you created in the previous steps, enter the following code to create an <code>else if</code> statement:
=======
Immediately after the closing <code>}</code> for the <code>if</code> statement you created in the previous steps, enter the following code to create a second <code>if</code> statement:
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
=======
Immediately after the closing <code>}</code> for the <code>if</code> statement you created in the previous steps, enter the following code to create a second <code>if</code> statement:
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43

<pre>
 else if (gameLocation[i] === "home") {
             paragraphs[1].innerHTML = "vs ";
<<<<<<< HEAD
<<<<<<< HEAD
             paragraphs[1].innerHTML += opponents[i];
 }//end of else if

=======
      }
 }
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
=======
      }
 }
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
</pre>
This statement creates an <code>else if</code> statement.  The <code>else if</code> statement provides code to be executed if the original condition evaluates to be false and the <code>gameLocation</code> value is <code>"home"</code>.  The <code>else if</code> statement provides an additional test to differentiate between <code>gameLocation</code> values of <code>"home"</code> and <code>""</code>.  If it is a "home" game this code will set the content to "vs".
</li>

<li>
In the first comment line before the start of the <code>addGameInfo()</code> functions, after the word "opponents", insert <b>gameLocation values</b>.  The following code shows the completed <code>addGameInfo()</code> function:
<pre>
// function to place opponents <mark>and gameLocation values </mark>in 
// second p element within each table data cell that has an id
function addGameInfo() {
   var paragraphs = "";
   for (var i = 0; i < 31; i++) {
      var date = i + 1;
      var tableCell = document.getElementById("08-" + date);
      paragraphs = tableCell.getElementsByTagName("p");
<<<<<<< HEAD
<<<<<<< HEAD
      paragraphs[1].innerHTML += opponents[i];<br>      
      <mark>if (gameLocation[i] === "away") {</mark>
            <mark>paragraphs[1].innerHTML = "@ ";</mark>
            <mark>paragraphs[1].innerHTML += opponents[i];</mark>
      <mark>}end of if </mark>
      <mark>else if (gameLocation[i] === "home") {</mark>
                <mark>paragraphs[1].innerHTML = "vs ";</mark>
                <mark>paragraphs[1].innerHTML += opponents[i];</mark>
           <mark>}//end of else if </mark><br>
      //end of for loop
}//end of addGameInfo function
=======
=======
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
      <mark>if (gameLocation[i] === "away") {</mark>
            <mark>paragraphs[1].innerHTML = "@ ";</mark>
      <mark>} </mark>
      <mark>else if (gameLocation[i] === "home") {</mark>
                <mark>paragraphs[1].innerHTML = "vs ";</mark>
           <mark>} </mark>
      <mark>}</mark>
      paragraphs[1].innerHTML <mark>+=</mark> opponents[i];
   }
}
<<<<<<< HEAD
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
=======
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
</pre>
</li>


<li>Reload the <b>calender.htm</b> and view the web page.  As you can see, <b>"vs"</b> followed by a space is now displayed before the opponent names in some of the table cells.  These dates correspond to the elements in the <code>gameLocation</code> array with a value of "home". </li>
<center><img src=".guides/img/SeminoleTrojan_Home.png" alt="Seminole Trojans" /></center>

<<<<<<< HEAD
<<<<<<< HEAD
<center><h1>Congratulations you have completed Assignment 5!</h1></center>
=======
<center><h1>Congratulations you have completed <br><b>PART 1</b> of Assignment 5!</h1></center>
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
=======
<center><h1>Congratulations you have completed <br><b>PART 1</b> of Assignment 5!</h1></center>
>>>>>>> 72eb571e27327498cb5316204990ca7d603aea43
