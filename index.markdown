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
<style>
.ui-sortable {
    width: 1000px;
}    
</style>
    
<!-- End of scripting functions! -->
    
We can use the ideas of AND, OR, and NOT that we learned in our logic gates lesson and apply them to our p5js programming! Instead of using AND, OR, and NOT gates, we use AND, OR and NOT operators in our programs. These operators will let us combine boolean expressions to make more complex if statements. 

# NOT Operator

The NOT operator acts just like the NOT logic gate: it takes in a boolean value and spits out the opposite boolean value. If you input true, it will output false, and if you input false, it will output true. The NOT operator in p5js is the exclamation point: <code>!</code>. We've actually already USED the not operator in our Card Collector assignment from the beginning of the semester <br>

Let's look at an example. If we had a boolean variable  <code> isCitizen</code> , we could write code to check if this person can vote like so:
<pre><code>
if(isCitizen){
    console.log("This person can vote");
}    
else{
    console.log("This person cannot vote");
}
</code></pre>

But we could have also written the same code using the not operator, like so:

<pre><code>
if(!isCitizen){
    console.log("This person cannot vote");
}    
else{
    console.log("This person can vote");
}
</code></pre>

Note that we can use the NOT operator on boolean expressions, not just boolean variables. For example, if we had a variable named <code>age</code> and we wanted to make sure someone was at least 18 to vote, we could write our code like this:
<pre><code>
if(age >=18){
    console.log("This person can vote");
}    
else{
    console.log("This person cannot vote");
}
</code></pre>

But we could have also written this code to use the not operator, like so:

<pre><code>
if(!(age >=18)){
    console.log("This person cannot vote");
}    
else{
    console.log("This person can vote");
}
</code></pre>
Note that we had to put the expression <code> age >=18</code> in brackets so that it would evalute BEFORE the NOT gate was applied. If you do not have the brackets, your code will not give you an error but your code will not behave the way you expect it to. It's best to wrap arithmetic boolean expressions like this in brackets before using the NOT operator.<br>

Now, in this case, the first example is much more intuitive and easier to read. We would never advocate using the not code for these examples. But in some cases, code using the negative can be clearer or more intuitive for the reader. For example, imagine you had a butler robot who would pour you juice while you worked on your brilliant computer projects. You might program the robot with logic like this:
<pre><code>
if(! isFull){
    pourJuice();
}
</pre><code>
    
In this case, the negative makes intuitve sense. Using the not operator makes it clearer what the context for when to pour Juice is. All this is to say that you can often avoid using the NOT operator, but sometimes it makes more "sense" to use it. 


[Next](./parsons/OR.html)
