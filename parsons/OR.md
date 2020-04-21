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


# OR Operator

Just like our AND and NOT operators, the OR operator behaves just like the OR game from our logic gate lesson. The OR operator takes in two boolean values and spits out <code> true</code> if either of its inputs is true, otherwise it spits out <code> false</code>. The OR operator in p5js is two bars <code> || </code>.  The bar key on your keyboard is the right side of your main keyboard, between your delete/backspace and return/enter keys. See image below for help finding the bar key. You need to press SHIFT to get the bar character. <br><br> 

<img src="../assets/keyboard.png">

Imagine our class was going on a field trip. Students can only go on the trip, if they have a field trip formed filled out. The only exception is students who are over the age of 18 and no longer need their parents permission. Code that expresses the logic of deciding if a student can attend the field trip could look like this:

<pre><code>
if( age >18 || hasForm){
    console.log("Student can attend field trip");
}
else{
    console.log("Student cannot attend field trip");
}
</code></pre>

Note, there is more than one way we could achieve the same behaviour. For example, we could avoid using OR operators by doing the following:

<pre><code>
if( age >18){
    console.log("Student can attend field trip");
}
else if (hasForm){
    console.log("Student can attend field trip");
}
else{
    console.log("Student cannot attend field trip");
}
</code></pre>

It is possible to avoid using OR operators, but it usually makes our code longer and with more else if statements with the same outputs. 

## Exercise
Imagine you are somewhat a somewhat forgetful person. You are frequently forgetting your wallet and keys when you leave the house. You decide to make yourself a "safe to leave the house detector". You put an RFID emmiter on your keys and in your wallet and install a small microprocessor at your door that checks, everytime the door is opened, whether or not your keys & wallet are going through the door.  Assume you have boolean variables <code>haveKeys </code> and  <code>haveWallet</code>. Write code that will appropriate call a  <code>soundAlarm()</code> function if you're trying to leave the house unprepared! Try solving it using an OR gate. Then try solving it using an AND gate instead. 

<button onClick="myFunction('hintKeys')"> Show Hint </button>

<div id='hintKeys' style="display:none;" >
<pre><code>
You can use the NOT operator to check if someone does NOT have their keys...
</code></pre>
</div>


<button onClick="myFunction('exKeysOR')"> Show OR Solution </button>

<div id='exKeysOR' style="display:none;" >
<pre><code>
if(!haveKeys || !haveWallet){
    soundAlarm()
}
</code></pre>
</div>

<button onClick="myFunction('exKeysAND')"> Show AND Solution </button>

<div id='exKeysAND' style="display:none;" >
<pre><code>
if(!(haveKeys && haveWallet)){
    soundAlarm()
}
</code></pre>
</div>

From the previous example, you will likely have discovered that we can mix our gates all together. We can use a NOT gate as part of our logic in addition to using an OR or an AND gate. You can also use OR and AND gates together.<br>

 For example, think back to our hiking example from our previous if/else notes package. We wanted to tell someone they could go hiking ONLY IF they had hiking boots and it was either sunny out or they had a rain coat. We accomplished this using nested if statements like so:
 
 <pre><code>
if(haveBoots){
    if(isSunny){
        console.log("You can go hiking!");
    }
    else if(haveRaincoat){
         console.log("You can go hiking!");
    }
    else{
        console.log("You cannot go hiking!");
    }
}
else{
    console.log("You cannot go hiking!");
}   
</code></pre>
 
Bleah. Look at all those if/else statements. What a mess to read! We could simplify this logic, by using the following AND and OR logic:

 <pre><code>
if(haveBoots && (isSunny || haveRaincoat){
    console.log("You can go hiking!");    
}
else{
    console.log("You cannot go hiking!");
}   
</code></pre>

That's much neater! One thing that is important to note is the brackets around our OR statement. Just like in math, where our operators have an ordering (remember:BEDMAS), our logical operators have an order. The order is: BRACKETS, NOT, AND, OR. I think of Nando's chicken to remember because it's N(ot)ANDO(r). What this means is if we don't put brackets in, our code would check <code> haveBoots && isSunny</code> first and then check <code> || haveRaincoat</code>. In this particular example, the behaviour is still the same, but it is something you need to be careful of. 

## Exercise



[Previous](./AND.html)
<!-- [Next](./elseif.html) -->
