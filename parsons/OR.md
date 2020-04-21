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

## Exercise
Imagine you are somewhat a somewhat forgetful person. You are frequently forgetting your wallet and keys when you leave the house. You decide to make yourself a "safe to leave the house detector". You put an RFID emmiter on your keys and in your wallet and install a small microprocessor at your door that checks, everytime the door is opened, whether or not your keys & wallet are going through the door.  Assume you have boolean variables <code>haveKeys </code> and  <code>haveWallet</code>. Write code that will appropriate call a  <code>soundAlarm()</code> function if you're trying to leave the house unprepared!

<button onClick="myFunction('exKeys')"> Show Solution </button>

<div id='exKeys' style="display:none;" >
<pre><code>
if(!haveKeys || !haveWallet){
    soundAlarm()
}
</code></pre>
</div>

[Previous](https://ms-hackman.github.io/AndOrNotes/)
<!-- [Next](./elseif.html) -->
