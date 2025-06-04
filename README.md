<html lang="zh-TW">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>圖卡抽籤</title>
<style>
  body {
    font-family: "Noto Sans TC", sans-serif;
    background: #fafafa;
    text-align: center;
    padding: 30px;
  }
  button {
    padding: 15px 35px;
    font-size: 20px;
    border-radius: 8px;
    border: none;
    background-color: #6a4c93;
    color: white;
    cursor: pointer;
    margin-bottom: 30px;
  }
  button:hover {
    background-color: #563d7c;
  }
  #card {
    max-width: 90vw;
    max-height: 70vh;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  }
</style>
</head>
<body>

<h1>線上圖卡抽籤</h1>
<button onclick="drawCard()">抽一張圖卡</button>
<br />
<img id="https://www.notion.so/_assets/app-de29758654f9d2ab.css" src="" alt="請點擊抽籤" />

<script>
  const cards = [
    "https://drive.google.com/file/d/1LBT9mJf7D18ctq_Jki02zRUb-JeDhIXE/view?usp=drive_link",
    "https://drive.google.com/file/d/1l7Zwb_UO-S7CerhTqzOlJZ4jPz_s_OZt/view?usp=sharing",
    "https://drive.google.com/file/d/1siTDmX85aOG-OB06eUoKrrnYIB7fULJp/view?usp=drive_link",
      ];

  function drawCard() {
    const idx = Math.floor(Math.random() * cards.length);
    const img = document.getElementById("card");
    img.src = cards[idx];
  }
</script>

</body>
</html>
