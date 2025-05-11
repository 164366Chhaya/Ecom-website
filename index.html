<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Brick Breaker</title>
  <style>
    body {
      margin: 0;
      background: #000;
      color: #fff;
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    canvas {
      background: #222;
      border: 2px solid #fff;
      margin-top: 10px;
    }
    .controls {
      margin-top: 10px;
    }
    .btn {
      padding: 10px 20px;
      margin: 0 10px;
      font-size: 20px;
      background: #fff;
      color: #000;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h2>Brick Breaker</h2>
  <canvas id="gameCanvas" width="480" height="320"></canvas>
  <div class="controls">
    <button class="btn" id="leftBtn">← Left</button>
    <button class="btn" id="rightBtn">Right →</button>
  </div>

  <script>
    const canvas = document.getElementById("gameCanvas");
    const ctx = canvas.getContext("2d");

    let ballX = canvas.width / 2;
    let ballY = canvas.height - 30;
    let ballRadius = 8;
    let dx = 2;
    let dy = -2;

    const paddleHeight = 10;
    const paddleWidth = 75;
    let paddleX = (canvas.width - paddleWidth) / 2;
    let rightPressed = false;
    let leftPressed = false;

    const brickRowCount = 5;
    const brickColumnCount = 7;
    const brickWidth = 60;
    const brickHeight = 20;
    const brickPadding = 10;
    const brickOffsetTop = 30;
    const brickOffsetLeft = 35;

    const bricks = [];
    for (let c = 0; c < brickColumnCount; c++) {
      bricks[c] = [];
      for (let r = 0; r < brickRowCount; r++) {
        bricks[c][r] = { x: 0, y: 0, status: 1 };
      }
    }

    let score = 0;

    // Keyboard controls
    document.addEventListener("keydown", (e) => {
      if (e.key === "ArrowRight") rightPressed = true;
      if (e.key === "ArrowLeft") leftPressed = true;
    });

    document.addEventListener("keyup", (e) => {
      if (e.key === "ArrowRight") rightPressed = false;
      if (e.key === "ArrowLeft") leftPressed = false;
    });

    // Mobile touch buttons
    document.getElementById("leftBtn").addEventListener("touchstart", () => leftPressed = true);
    document.getElementById("leftBtn").addEventListener("touchend", () => leftPressed = false);
    document.getElementById("rightBtn").addEventListener("touchstart", () => rightPressed = true);
    document.getElementById("rightBtn").addEventListener("touchend", () => rightPressed = false);

    function drawBall() {
      ctx.beginPath();
      ctx.arc(ballX, ballY, ballRadius, 0, Math.PI * 2);
      ctx.fillStyle = "#f00";
      ctx.fill();
      ctx.closePath();
    }

    function drawPaddle() {
      ctx.beginPath();
      ctx.rect(paddleX, canvas.height - paddleHeight, paddleWidth, paddleHeight);
      ctx.fillStyle = "#0f0";
      ctx.fill();
      ctx.closePath();
    }

    function drawBricks() {
      for (let c = 0; c < brickColumnCount; c++) {
        for (let r = 0; r < brickRowCount; r++) {
          if (bricks[c][r].status === 1) {
            const brickX = c * (brickWidth + brickPadding) + brickOffsetLeft;
            const brickY = r * (brickHeight + brickPadding) + brickOffsetTop;
            bricks[c][r].x = brickX;
            bricks[c][r].y = brickY;
            ctx.beginPath();
            ctx.rect(brickX, brickY, brickWidth, brickHeight);
            ctx.fillStyle = "#ff0";
            ctx.fill();
            ctx.closePath();
          }
        }
      }
    }

    function drawScore() {
      ctx.font = "16px Arial";
      ctx.fillStyle = "#fff";
      ctx.fillText("Score: " + score, 8, 20);
    }

    function collisionDetection() {
      for (let c = 0; c < brickColumnCount; c++) {
        for (let r = 0; r < brickRowCount; r++) {
          const b = bricks[c][r];
          if (b.status === 1) {
            if (
              ballX > b.x &&
              ballX < b.x + brickWidth &&
              ballY > b.y &&
              ballY < b.y + brickHeight
            ) {
              dy = -dy;
              b.status = 0;
              score++;
              if (score === brickRowCount * brickColumnCount) {
                alert("YOU WIN!");
                document.location.reload();
              }
            }
          }
        }
      }
    }

    function draw() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      drawBricks();
      drawBall();
      drawPaddle();
      drawScore();
      collisionDetection();

      // Ball bounce
      if (ballX + dx > canvas.width - ballRadius || ballX + dx < ballRadius) {
        dx = -dx;
      }
      if (ballY + dy < ballRadius) {
        dy = -dy;
      } else if (ballY + dy > canvas.height - ballRadius) {
        if (ballX > paddleX && ballX < paddleX + paddleWidth) {
          dy = -dy;
        } else {
          alert("GAME OVER");
          document.location.reload();
        }
      }

      ballX += dx;
      ballY += dy;

      // Paddle movement
      if (rightPressed && paddleX < canvas.width - paddleWidth) {
        paddleX += 5;
      } else if (leftPressed && paddleX > 0) {
        paddleX -= 5;
      }

      requestAnimationFrame(draw);
    }

    draw();
  </script>
</body>
</html>
