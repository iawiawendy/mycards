<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <title>抽一張卡</title>
  <style>
    body {
      font-family: '微軟正黑體', sans-serif;
      text-align: center;
      padding: 50px;
      background-color: #f9f9f9;
    }
    h1 {
      color: #333;
    }
    button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #8ecae6;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #219ebc;
    }
    #result {
      margin-top: 30px;
    }
    img {
      max-width: 100%;
      height: auto;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    }
  </style>
</head>
<body>

  <h1>抽一張圖卡吧！</h1>
  <button onclick="drawCard()">🎴 抽卡</button>

  <div id="result"></div>

  <script>
    const cards = [
      "https://drive.google.com/uc?export=view&id=1PS2nyGqu0PekwOk-YH9I9yq_E9AxWIK4", 
      "https://i0.wp.com/janstockcoin.com/wp-content/uploads/2021/06/pexels-photo-747964-scaled.jpeg?fit=2560%2C1616&ssl=1",
      "https://www.notion.so/1ed0c329cd8f8098bd28c3da90231f4c?source=copy_link#2080c329cd8f808a9489d58ee5b33993"
    ];

    function drawCard() {
      const index = Math.floor(Math.random() * cards.length);
      const imageUrl = cards[index];
      document.getElementById('result').innerHTML = `<img src="${imageUrl}" alt="抽到的卡">`;
    }
  </script>

</body>
</html>
