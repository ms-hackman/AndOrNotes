---
layout: default
description:  
---

<!-- Function for hiding code!  -->
<script>
    function myFunction(name) {
      var x = document.getElementById(name);
      if (x.style.display === "none") {
        x.style.display = "block";
      } 
      else if(x.style.display ==="first"){
          x.style.display="none";         
      }
      else {
        x.style.display = "none";
      }
    }    
</script>
<!-- End of scripting functions! -->
<style>
.ui-sortable {
    width: 1000px;
}    
</style>

# AND operator
Just like with our AND gate,  the AND operator  takes in two true or false inputs and spits out true if both inputs were true, otherwise it spits out false. The AND operator in p5js is two ampersands <code> && </code>. <br><br>

For example, imagine Ms. Hackman was planning on ordering some donuts to share with the class. She wants to make sure she orders enough donuts so each student gets at least 1 donut. She also has a budget of $100 and donuts cost $5 apiece. Given variables <code> numDonuts</code> and <code> numStudents</code>, we could write code, using nested if statements, to determine if Ms. Hackman has ordered an apppriate number of donuts:
<pre>
<code>
if(numDonuts >= numStudents){
    if(numDonuts*5 <= 100){
        console.log("Accept Donut Order");
    }
    else{
        console.log("Reject Donut Order");
    }
}
else{
    console.log("Reject Donut Order");
}
</code>
</pre>

This code works. The first if statement checks that the number of donuts is more than the number of students (so each student gets at least one donut). The second if statement checks that the order hasn't gone over budget (by making sure the total cost is less than $100). It only accepts the donut order if BOTH statements are true, otherwise it rejects the donut order. But notice that this code needs two separate else conditions for rejecting an order? This code just isn't very "elegant". We could simplify the code by using an AND operator:

<pre><code>
if(numDonuts >= numStudents && numDonuts*5 <=100){
    console.log("Accept Donut Order");
}
else{
    console.log("Reject Donut Order");
}
</code></pre>

The <code>&&</code> operator takes two boolean expressions: one to its left and the other to its right. If both are true, it will return true, otherwise it returns false. <br>

Note that we can always rewrite code that uses the AND operator with nested if statements. But the AND operator code is shorter, neater, and easier to read. 

## Exercise
Imagine there is a special scholarship for CS 10 students whose average is over 80%. Using the variable <code> grade </code> (which stores the student's average grade) and the boolean variable <code>tookCS10</code>, write code that uses the && operator to print out the message "Elligible for scholarship" if a student is elligible. 

<button onClick="myFunction('scholarshipex')"> Show Solution </button>

<div id='scholarshipex' style="display:none;" >
<pre><code>
if(grade > 80 && tookCS10){
    console.log("Elligible for scholarship!");
}
</code></pre>
</div>

## Using more than one AND 

We can "chain" together boolean expressions using multiple AND oprators. For example, say we wanted to call someone a SCIENCE ROCKSTAR if they took all four Sciences (bio, chem, physics and COMPUTER SCIENCE :D :D :D ), we could use the following logic:
<pre><code>
if(tookBio && tookChem && tookPhysics && tookCS){
    console.log("You are a SCIENCE ROCKSTAR!");
}
</code></pre>

This code is read from left to right: it first checks if they took Bio and Chem. If this is false, it immediately stops and doesn't check anything else. If they did take Bio and Chem, it then checks to see if they took Physics. If they did not take physics, it immediately stops. If they did take Bio, Chem, AND Physics, it will finally check if they took CS to determine whether or not they should be declared a SCIENCE ROCKSTAR! 

One common situation where we use && gates is when checking to see if a user has clicked on a rectangular object in our program. For example, consider the image of the following fake program:
<img src="/assets/example_button.jpg">

Note the x,y coordinates for the four corners of the button have been labelled. If we wanted to check if this button has been clicked we could use the following code:

<pre><code>
function mousePressed(){
    if(mouseX > = 70 && mouseX <= 270 && mouseY >= 100 && mouseY <= 150){
        console.log("Button has been clicked!");
    }
}
</code></pre>

## Example
Rewrite the "button clicked" code above to use the variables: <code> buttonX, buttonY, buttonW, buttonH</code> which represent the x and y coordinate of the top left corner, and the width and height of the button. 

<button onClick="myFunction('buttonEx1')"> Show Solution </button>

<div id='buttonEx1' style="display:none;" >
<pre><code>
function mousePressed(){
    if(mouseX > = buttonX && mouseX <= (buttonX + buttonW) && mouseY >= buttonY && mouseY <= (buttonY + buttonH)){
        console.log("Button has been clicked!");
    }
}
</code></pre>
</div>

<!-- Using Not gate -->
Note that we can combine AND gates and NOT gates to make more interesting logic. For example, this code:

<pre><code>
if()
</code></pre>

[Previous](https://ms-hackman.github.io/AndOrNotes/)
[Next](./OR.html)
