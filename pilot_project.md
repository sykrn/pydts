

# Pilot project testing

## Lihat score anda dengan memasukkan email
<input type="email" id="email" name="emails" placeholder="email netacad">
<button onclick="onClick()">Click Me</button>
<pre>
<div id="result" style="display:none;">

</div>
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
        var itemout = 'Items test cases: \n';
        var zip = obj[email]["out"].map(function(e, i) {
              return [e, obj[email]["scores"][i]];
         });
    
        for(i in zip){
            itemout += i[0]+'score: '+i[0]+'\n\n';
        }
    
        x.innerHTML=fscore+itemout;           
    }
    x.style.display = "block"; 
}
</script>

