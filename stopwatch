<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Stopwatch</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    background-color: #f5eded;
  }
  .container {
    margin-top: 50px;
  }
  .stopwatch {
    font-size: 24px;
    margin-bottom: 20px;
  }
  .btn {
    padding: 20px 40px;
    font-size: 20px;
    cursor: pointer;
    background-color: #4CAF50;
    color: #fff;
    border: none;
    border-radius: 5px;
    margin-right: 10px;
  }
  .btn:hover {
    background-color: #45a049;
  }
</style>
</head>
<body>
<div class="container">
  <h1>Stopwatch</h1>
  <div class="stopwatch">00:00:00</div>
  <button class="btn" onclick="startStopwatch()">Start</button>
  <button class="btn" onclick="pauseStopwatch()">Pause</button>
  <button class="btn" onclick="resetStopwatch()">Reset</button>
</div>

<script>
  let stopwatchInterval;
  let hours = 0, minutes = 0, seconds = 0;

  function startStopwatch() {
    clearInterval(stopwatchInterval);
    stopwatchInterval = setInterval(updateStopwatch, 1000);
  }

  function pauseStopwatch() {
    clearInterval(stopwatchInterval);
  }

  function resetStopwatch() {
    clearInterval(stopwatchInterval);
    hours = 0;
    minutes = 0;
    seconds = 0;
    updateStopwatch();
  }

  function updateStopwatch() {
    seconds++;
    if (seconds >= 60) {
      seconds = 0;
      minutes++;
      if (minutes >= 60) {
        minutes = 0;
        hours++;
      }
    }
    const formattedTime = pad(hours) + ':' + pad(minutes) + ':' + pad(seconds);
    document.querySelector('.stopwatch').textContent = formattedTime;
  }

  function pad(number) {
    return (number < 10) ? '0' + number : number;
  }
</script>
</body>
</html>
