<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>!!! SYSTEM LOCKED !!!</title>
  <style>
    body {
      margin: 0;
      font-family: 'Courier New', monospace;
      background: black;
      color: red;
      text-align: center;
      padding-top: 100px;
    }
    h1 {
      font-size: 3em;
      text-shadow: 2px 2px 5px #ff0000;
      animation: blink 1s infinite;
    }
    @keyframes blink {
      50% { opacity: 0; }
    }
    .warning {
      font-size: 1.2em;
      margin-top: 20px;
      color: white;
    }
    .code {
      margin-top: 30px;
      font-size: 1.5em;
      color: #0f0;
      background: #111;
      padding: 15px;
      border-radius: 10px;
      display: inline-block;
    }
    button {
      margin-top: 40px;
      padding: 15px 30px;
      font-size: 1.2em;
      background: red;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      animation: blink 1.5s infinite;
    }
    button:hover {
      background: darkred;
    }
  </style>
</head>
<body>
  <h1>⚠ SYSTEM LOCKED ⚠</h1>
  <div class="warning">
    Semua file Anda telah dienkripsi! <br>
    Untuk mengembalikannya, masukkan <b>KODE RAHASIA</b>.
  </div>

  <div class="code">KODE: <span id="fakeCode">########</span></div>

  <div>
    <input type="text" id="inputCode" placeholder="Masukkan kode..." style="margin-top:30px; padding:10px; font-size:1em;">
  </div>
  <button onclick="unlock()">UNLOCK</button>

  <script>
    // kode rahasia untuk prank
    const secretCode = "1234";

    function unlock() {
      const input = document.getElementById("inputCode").value;
      if (input === secretCode) {
        document.body.innerHTML = `
          <h1 style="color:lime;">✅ Sistem Dipulihkan ✅</h1>
          <p style="color:white; font-size:1.2em;">Hahaha, ini cuma prank! 😆</p>
        `;
      } else {
        alert("❌ Kode salah! Coba lagi.");
      }
    }

    // Efek generate kode palsu
    setInterval(() => {
      document.getElementById("fakeCode").textContent =
        Math.random().toString(36).substring(2, 10).toUpperCase();
    }, 1000);
  </script>
</body>
</html>
