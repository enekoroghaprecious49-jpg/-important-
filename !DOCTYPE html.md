<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine 💖</title>
  <style>
    body {
      background-color: #ffe6eb;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0 10px 20px rgba(0,0,0,0.1);
    }
    button {
      padding: 10px 20px;
      border: none;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      margin: 10px;
    }
    #yes {
      background-color: #4CAF50;
      color: white;
    }
    #no {
      background-color: #f44336;
      color: white;
      position: absolute;
    }
  </style>
</head>
<body>

<div class="card">
  <h2>Hey Cutie 🥰</h2>
  <p>Will you be my Valentine? 💕</p>
  <button id="yes" onclick="yesClicked()">Yes 💖</button>
  <button id="no" onmouseover="moveNo()">No 😏</button>
</div>

<script>
  function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
  }

  function yesClicked() {
    document.body.innerHTML = "<h1 style='color:#ff4d6d;'>YAYYY 💖 I knew it 😍</h1>";
  }
</script>

</body>
</html>
<script>
  const noTexts = [
    "No 😏",
    "Don’t say no 🥺",
    "Please baby 🙏",
    "Are you sure? 😭",
    "HAHA YOU CAN’T SAY NO 😂",
    "My heart 💔",
    "Okay last chance 😳"
  ];

  let count = 0;

  function moveNo() {
    const noBtn = document.getElementById("no");

    const x = Math.random() * (window.innerWidth - 120);
    const y = Math.random() * (window.innerHeight - 60);

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";

    noBtn.innerText = noTexts[count % noTexts.length];
    count++;
  }

  function yesClicked() {
    document.body.innerHTML = `
      <div style="text-align:center; margin-top:40vh;">
        <h1 style="color:#ff4d6d;">YAYYY 💖💖💖</h1>
        <p>You just made me the happiest person 😍</p>
      </div>
    `;
  }
</script>
