<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Birthday Decorations with Flowers</title>
  <style>
    /* General Page Styling */
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      background: white;
      overflow: hidden;
      font-family: 'Arial', sans-serif;
    }

    /* Butterfly Styling */
    .butterfly {
      position: absolute;
      width: 50px;
      height: 50px;
      background-image: url('https://img.icons8.com/ios/452/butterfly.png');
      background-size: contain;
      background-repeat: no-repeat;
      animation: floatUp 10s ease-in-out infinite;
    }

    @keyframes floatUp {
      0% {
        transform: translateX(0) translateY(100vh);
      }
      100% {
        transform: translateX(50px) translateY(-100vh);
      }
    }

    /* Flower Decoration Styling */
    .flower {
      position: absolute;
      width: 80px;
      height: 80px;
      background-image: url('https://img.icons8.com/ios/452/flower.png');
      background-size: contain;
      background-repeat: no-repeat;
    }

    .flower.top-left { top: 10%; left: 10%; }
    .flower.top-right { top: 10%; right: 10%; }
    .flower.bottom-left { bottom: 10%; left: 10%; }
    .flower.bottom-right { bottom: 10%; right: 10%; }

    /* Enhanced Message Box Styling */
    .message-box {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 400px;
      padding: 30px;
      background: linear-gradient(135deg, #ffffff, #e0d1f9);
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
      text-align: center;
      color: #4c257a;
      z-index: 1000;
    }

    .message-box h2 {
      margin: 0 0 10px;
      font-size: 26px;
      color: #6a0dad;
      text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
    }

    .message-box p {
      margin: 0 0 20px;
      font-size: 16px;
      color: #4c257a;
    }

    .message-box button {
      padding: 12px 25px;
      font-size: 16px;
      color: white;
      background: linear-gradient(90deg, #ff7eb3, #ff758c);
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 6px 15px rgba(255, 117, 140, 0.5);
      transition: all 0.3s ease;
    }

    .message-box button:hover {
      transform: scale(1.1);
      background: linear-gradient(90deg, #ff758c, #ff7eb3);
      box-shadow: 0 8px 20px rgba(255, 117, 140, 0.8);
    }

    .message-box button:active {
      transform: scale(0.95);
      box-shadow: 0 4px 10px rgba(255, 117, 140, 0.5);
    }

    /* Birthday Decorations Styling */
    .birthday-decorations {
      display: none;
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 100;
      background: linear-gradient(45deg, #e0c1ff, #f8c7d9);
      text-align: center;
      color: #4c257a;
    }

    .birthday-decorations h1 {
      margin-top: 20px;
      font-size: 50px;
      font-weight: bold;
      color: #ffffff;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), 0 0 15px #ffffff;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), 0 0 10px #ffffff;
      }
      to {
        text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3), 0 0 25px #ff69b4;
      }
    }

    .birthday-decorations img {
      margin-top: 20px;
      width: 300px;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
    }

    /* Cake Styling */
    .cake {
      position: absolute;
      bottom: -250px; /* Initially hidden below the screen */
      left: 50%;
      transform: translateX(-50%);
      width: 300px;
      height: 200px;
      background-image: url('https://img.icons8.com/ios/452/cake.png');
      background-size: contain;
      background-repeat: no-repeat;
      display: none; /* Initially hidden */
    }

    /* Cake Animation */
    @keyframes slideUp {
      0% {
        bottom: -250px;
      }
      100% {
        bottom: 50%;
      }
    }

    /* Button Styling for Cake */
    .birthday-decorations button {
      margin-top: 20px;
      padding: 12px 25px;
      font-size: 16px;
      color: white;
      background: linear-gradient(90deg, #ff7eb3, #ff758c);
      border: none;
      border-radius: 30px;
      cursor: pointer;
      box-shadow: 0 6px 15px rgba(255, 117, 140, 0.5);
      transition: all 0.3s ease;
    }

    .birthday-decorations button:hover {
      transform: scale(1.1);
      background: linear-gradient(90deg, #ff758c, #ff7eb3);
      box-shadow: 0 8px 20px rgba(255, 117, 140, 0.8);
    }

    .birthday-decorations button:active {
      transform: scale(0.95);
      box-shadow: 0 4px 10px rgba(255, 117, 140, 0.5);
    }
  </style>
</head>
<body>
  <!-- Floating Butterflies -->
  <div class="butterfly" style="left: 10%; animation-delay: 0s;"></div>
  <div class="butterfly" style="left: 30%; animation-delay: 2s;"></div>
  <div class="butterfly" style="left: 50%; animation-delay: 4s;"></div>
  <div class="butterfly" style="left: 70%; animation-delay: 6s;"></div>
  <div class="butterfly" style="left: 90%; animation-delay: 8s;"></div>
  <div class="butterfly" style="left: 20%; animation-delay: 3s;"></div>
  <div class="butterfly" style="left: 60%; animation-delay: 5s;"></div>

  <!-- Flower Decorations in the corners -->
  <div class="flower top-left"></div>
  <div class="flower top-right"></div>
  <div class="flower bottom-left"></div>
  <div class="flower bottom-right"></div>

  <!-- Enhanced Message Box -->
  <div class="message-box">
    <h2>Welcome to the Butterfly Wonderland!</h2>
    <p>Click the button to celebrate the birthday!</p>
    <button onclick="startBirthdayDecorations()">Celebrate Now</button>
  </div>

  <!-- Birthday Decorations Container -->
  <div class="birthday-decorations">
    <h1>Happy Birthday! 🎉</h1>
    <img src="birthday.jpg" alt="Birthday Celebration Photo">
    <button onclick="showCake()">Let's Cut the Cake</button>
  </div>

  <!-- Cake Image -->
  <div class="cake" id="cake"></div>

  <script>
    function startBirthdayDecorations() {
      document.querySelector('.message-box').style.display = 'none';
      document.querySelectorAll('.butterfly').forEach(b => b.style.display = 'none');
      document.querySelector('.birthday-decorations').style.display = 'block';
    }

    function showCake() {
      const cake = document.getElementById('cake');
      cake.style.display = 'block'; // Show the cake
      cake.style.animation = 'slideUp 3s ease-out forwards'; // Trigger cake animation
    }
  </script>
</body>
</html>
