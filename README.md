# my.pesan-romantis
Pesan romantis 
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Pesan Romantis</title>
  <style>
    body {
      background-color: #111;
      color: #ff6ec7;
      font-family: 'Courier New', monospace;
      text-align: center;
      padding-top: 50px;
    }
    .teks {
      font-size: 2rem;
      white-space: pre;
    }
    .hati {
      font-size: 16px;
      line-height: 1;
      margin-top: 30px;
      display: none;
      white-space: pre;
    }
  </style>
</head>
<body>
  <div id="output" class="teks"></div>
  <pre id="hati" class="hati">
   ***     ***   
  ******* ******* 
 *************** 
  *************  
   ***********   
    *********    
     *******     
      *****      
       ***       
        *        
  </pre>

  <script>
    const teks = ["Saya", "Suka", "Kamu"];
    let output = document.getElementById("output");
    let hati = document.getElementById("hati");

    async function tampilkan() {
      for (let kata of teks) {
        output.textContent = "";
        for (let i = 0; i < kata.length; i++) {
          output.textContent += kata[i];
          await new Promise(r => setTimeout(r, 150));
        }
        await new Promise(r => setTimeout(r, 500));
      }
      hati.style.display = "block";
    }

    tampilkan();
  </script>
</body>
</html>
