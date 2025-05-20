<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Birthday Sister</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to top right, #ffe6f0, #ffe0cc);
      overflow: hidden;
    }

    .container {
      text-align: center;
      padding: 50px;
      color: #d63384;
      z-index: 2;
      position: relative;
    }

    h1 {
      font-size: 3em;
      margin-bottom: 0.3em;
      animation: fadeIn 2s ease-out;
    }

    p {
      font-size: 1.3em;
      line-height: 1.6;
      max-width: 600px;
      margin: 0 auto;
      animation: fadeIn 3s ease-out;
    }

    .balloon {
      position: absolute;
      width: 60px;
      height: 80px;
      background: pink;
      border-radius: 50% 50% 50% 50%;
      animation: float 6s infinite ease-in-out;
      opacity: 0.8;
    }

    .balloon::before {
      content: '';
      position: absolute;
      width: 2px;
      height: 40px;
      background: #999;
      top: 80px;
      left: 29px;
    }

    @keyframes float {
      0% { transform: translateY(100vh); }
      100% { transform: translateY(-120vh); }
    }

    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(20px); }
      100% { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Happy Birthday, Sis!</h1>
    <p>
      Dear Sister,<br><br>
      On your special day, I just want to remind you how much you're loved and cherished. You light up our lives with your smile and kindness. May your year be full of joy, laughter, and all your dreams coming true.
      <br><br>
      Love you always!
    </p>
  </div>

  <script>
    // Create balloons
    for (let i = 0; i < 20; i++) {
      let balloon = document.createElement('div');
      balloon.className = 'balloon';
      balloon.style.left = Math.random() * 100 + 'vw';
      balloon.style.animationDuration = (5 + Math.random() * 5) + 's';
      balloon.style.background = `hsl(${Math.random() * 360}, 70%, 80%)`;
      document.body.appendChild(balloon);
    }
  </script>
</body>
</html>
