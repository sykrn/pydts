

# Pilot project testing

### Lihat score anda dengan memasukkan email
contoh: 'abcd@gmail.com'

<input type="email" id="email" name="emails" placeholder="email netacad">
<button onclick="onClick()">Cari</button>
<pre>
<code>
<div id="result">

</div>
</code>
</pre>



<script>
import obj from './p1_pilot.json';
function onClick() {
    var x = document.getElementById("result");    
    var email = document.getElementById("email").value;
    var notexist = typeof obj[email]=== "undefined";
    if (notexist){
       x.innerHTML='Email ID Tidak ditemukan';
    } 
    else{
        var fscore = 'Email: '+email+'\nFinal Score : ' + obj[email]["score"]+"\n\n";
        var itemout = 'Items test cases: \nformat result:[scorer,expected value(s),expected dtype,your value(s),your dtype]\n======================================\n';
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

