

# Latihan SBA (Nilai Remedi belum diupload ke netacad)

### Lihat score anda dengan memasukkan email -- Data Final
contoh: 'abcd@gmail.com'

<script  src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.0.0/core.min.js"></script>
<script  src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.0.0/sha1.min.js"></script>
<script type="text/javascript" src="lsba.json"></script>

<input type="email" id="email" name="emails" placeholder="email netacad">
<button onclick="onClick()">Cari</button>
<pre>
<code>
<div id="result">

</div>
</code>
</pre>


<script>
function onClick() {
    var x = document.getElementById("result");    
    var email = document.getElementById("email").value;
    var ehash = CryptoJS.SHA1(email);    
    var notexist = typeof obj[ehash]=== "undefined";
    if (notexist){
       ser = obj[CryptoJS.SHA1("error")].split("\n").sort().join("\n");
       x.innerHTML='Email ID Tidak ditemukan atau kode anda mengandung error!!\n\nList error:\n'+ser;
    } 
    else{
        var fscore = 'Email: '+email+' -- priority: '+obj[ehash]["priority"]+'\nFinal Score : ' + obj[ehash]["score"]+"\n\n";
        var itemout = 'Items test cases: \nformat result:[scorer,expected value(s),expected dtype,your value(s),your dtype]\n======================================\n';
        var o = obj[ehash]["out"]; 
        for(i=0;i<o.length;i++){
            ox = o[i].split("<").join("type ");
            ox = ox.split(">").join("");
            itemout += ox+">>>>>Item score: "+obj[ehash]["scores"][i]+"\n\n";
        }
        x.innerHTML=fscore+itemout;           
    }
    x.style.display = "block"; 
}
</script>

