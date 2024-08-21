<html lang="zxx">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box !important;
    }

    html, body {
      height: 100%;
    }

    body {
      display: table;
      width: 100%;
      height: 100%;
      background-color: #171717;
      color: #000;
      line-height: 1.6;
      position: relative;
      font-family: sans-serif;
      overflow: hidden;
    }

    .lines {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 100%;
      margin: auto;
      width: 90vw;
    }

    .line {
      position: absolute;
      width: 1px;
      height: 100%;
      top: 0;
      left: 50%;
      background: rgba(255, 255, 255, 0.1);
      overflow: hidden;
    }

    .line::after {
      content: '';
      display: block;
      position: absolute;
      height: 15vh;
      width: 100%;
      top: -50%;
      left: 0;
      background: linear-gradient(to bottom, rgba(255, 255, 255, 0) 0%, #ffffff 75%, #ffffff 100%);
      animation: drop 2s 0s infinite;
      animation-fill-mode: forwards;
      animation-timing-function: cubic-bezier(0.9, 0.40, 0, 1);
    }

    .line:nth-child(1) {
      margin-left: -25%;
    }

    .line:nth-child(1)::after {
      animation-delay: 2s;
    }

    .line:nth-child(3) {
      margin-left: 25%;
    }

    .line:nth-child(3)::after {
      animation-delay: 0s;
    }

    @keyframes drop {
      0% {
        top: -50%;
      }
      100% {
        top: 110%;
      }
    }
  </style>
</head>
<body>
  <div class="lines">
    <div class="line"></div>
    <div class="line"></div>
    <div class="line"></div>
  </div>
</body>
</html>
