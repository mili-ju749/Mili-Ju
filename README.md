index.html
<!DOCTYPE html>
<html>
<head>
  <title>Mili Ju – Write & Earn</title>
  <style>
    body {
      background: #f4f4f4;
      font-family: Arial;
      padding: 30px;
      text-align: center;
    }
    h1 {
      color: #4CAF50;
    }
    textarea {
      width: 80%;
      height: 200px;
      font-size: 16px;
      padding: 10px;
      margin-top: 20px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      margin-top: 15px;
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    .saved-text {
      margin-top: 20px;
      color: green;
    }
  </style>
</head>
<body>
  <h1>📝 Welcome to Mili Ju</h1>
  <p>Write your ideas, poems, quotes, or stories below and start your journey!</p>

  <textarea id="textInput" placeholder="Start writing here..."></textarea><br>
  <button onclick="saveText()">💾 Save Text</button>

  <p class="saved-text" id="message"></p>

  <script>
    function saveText() {
      const text = document.getElementById("textInput").value;
      if (text.trim() === "") {
        alert("Please write something!");
        return;
      }
      localStorage.setItem("miliJuText", text);
      document.getElementById("message").innerText = "✅ Your text is saved (on this device)!";
    }
  </script>
</body>
</html>
