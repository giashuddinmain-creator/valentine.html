<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💖</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: pink;
      font-family: Arial, sans-serif;
      text-align: center;
      overflow: hidden;
    }

    .box {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.2);
    }

    button {
      padding: 10px 25px;
      margin: 15px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    #yes {
      background: #ff4d6d;
      color: white;
    }

    #no {
      background: #ccc;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="box">
    <h1>Will you be my Valentine? 💕</h1>
    <button id="yes" onclick="yesClicked()">Yes ❤️</button>
    <button id="no" onmouseover="moveNo()">No 😝</button>
  </div>

  <script>
    function moveNo() {
      const noBtn = document.getElementById("no");
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 100);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    function yesClicked() {
      document.body.innerHTML = `
        <div style="text-align:center;">
          <h1>Yayyy! 💖🎉</h1>
          <p>You just made me the happiest 😍</p>
        </div>
      `;
    }
  </script>

</body>
</html>
