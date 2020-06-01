

# Pilot project testing

## Lihat score anda dengaan memasukkan email
<input type="email" id="email" name="emails" placeholder="email netacad">
<button onclick="onClick()">Click Me</button>
<pre>
<div id="result" style="display:none;">
</div>
</pre>

<script type="text/javascript" src="p1_pilot.json"></script>

<script>
function onClick() {
    var email = document.getElementById("email").value;
    var notexist = typeof obj[email]=== "undefined";    
    document.getElementById("result").innerHTML=obj[email]["out"];
    x.style.display = "block";      
    }
</script>

