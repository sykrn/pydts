

# Pilot project testing

## Lihat score anda dengan memasukkan email
<input type="email" id="email" name="emails" placeholder="email netacad">
<button onclick="onClick()">Click Me</button>
<pre>
<code>
<div id="result" style="display:none;">

</div>
</code>
</pre>

<script type="text/javascript" src="p1_pilot.json"></script>

<script>
function onClick() {
    var x = document.getElementById("result");    
    var email = document.getElementById("email").value;
    var notexist = typeof obj[email]=== "undefined";
    if (notexist){
       x.innerHTML='Email ID Tidak ditemukan';
    } 
    else{
        var fscore = 'Final Score: ' + obj[email]["score"]+"\n\n";
        var itemout = 'Items test cases: \n======================================\n';
        var o = obj[email]["out"]; 

        for(i=0;i<o.length;i++){
            ox = o[i].split("<").join("type ");
            ox = ox.split(">").join("");
            itemout += ox+">>>>>Item score: "+obj[email]["scores"][i]+"\n\n";
        }
    
        x.innerHTML=fscore+itemout;           
    }
    x.style.display = "block"; 
}
</script>

