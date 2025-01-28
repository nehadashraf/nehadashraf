<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Auto-Complete Name</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #f4f4f9;
    }
    .container {
      text-align: center;
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }
    input {
      width: 300px;
      padding: 10px;
      margin-top: 10px;
      font-size: 16px;
      border: 2px solid #ddd;
      border-radius: 6px;
      outline: none;
    }
    input:focus {
      border-color: #007bff;
    }
    .hint {
      color: #aaa;
      margin-top: 5px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Type Your Name</h1>
    <input type="text" id="nameInput" placeholder="Start typing..." />
    <p class="hint">Hint: Type "N" to see magic ✨</p>
  </div>

  <script>
    const fullName = "Nehad Ashraf";
    const inputField = document.getElementById("nameInput");

    inputField.addEventListener("input", (e) => {
      const userInput = e.target.value;
      if (fullName.toLowerCase().startsWith(userInput.toLowerCase())) {
        e.target.value = fullName.slice(0, userInput.length);
      }
    });
  </script>
</body>
</html>
