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
    
We can use the ideas of AND, OR, and NOT that we learned in our logic gates lesson and apply them to our p5js programming! Instead of using AND, OR, and NOT gates, we use AND, OR and NOT operators in our programs. These operators will let us combine boolean expressions to make more complex if statements. 

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



<!-- [Next](./parsons/else.html) -->
