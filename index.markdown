---
layout: default
title: Ms. Hackman's And/Or/Not Notes & Problems
description: Read the notes. Embeded in the notes are examples to try. <br>  After you've completed this, return to google classroom to do this week's quiz and assignment.
---
<!-- Function for hiding code!  -->
<script>
    function myFunction(name) {
      var x = document.getElementById(name);
      if (x.style.display === "none") {
        x.style.display = "block";
      } else {
        x.style.display = "none";
      }
    }    
</script>
<!-- End of scripting functions! -->
    
We’ve already seen simple uses of if statements in class but let’s review and get a bit more complex!
# If Statements
If statements allow us to run parts of our code only run when certain conditions are met. These “conditions” must be written as  <b>true or false</b>  statements. True or false statements are called  <b>boolean expressions .</b>

<code>
if(<i>boolean expression</i>){<br >
&nbsp;&nbsp;&nbsp;&nbsp; <i>code to run</i><br >
}  <br >
</code>


We refer to the if statement + boolean expression + code to run as an <b> if block.</b>


<!-- Hiding code test>
<button onClick="myFunction('code1')"> Hide Code 1 </button>

<div id='code1'>
<code>
console.log("Hello World");
</code>
</div>
<-->

    
Boolean expressions can be made up of any code that evaluates to <b> true or false </b>. Examples of boolean expressions include:

<code>
  X > 7 //is true if x is greater than 7, otherwise is false<br >
  Y <= 10 //is true if y is less than OR EQUAL TO 10, otherwise it is false<br>
  Z === 30 // checks if z is equal to 30. Note in p5js we use three equal signs to check if things are equal <br>
  A !== 17 // check if A is NOT equal to 17. Note in p5js we use two equal signs after the exclamation poitn <br>
</code>

<b>Note a boolean variable is ALREADY a boolean expression.</b> So the following code would actually display “Yes, Ms. Hackman is very very very cool.” (regardless of how true you think that statement actually is.

<code>
let isCool = true;<br >
if(isCool){<br >
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“Yes, Ms. Hackman is very very very cool.”);<br>
}<br>
</code>

The code we want to run if our if statement is true must live between two curly brackets {}. It is a common bug to forget one of your curly brackets, or to accidentally put code inside the brackets, you meant to be outside (or put code outside the brackets you meant to put inside), so be careful!


[Next](./parsons/else.html)
