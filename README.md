# queenklebsiella.github.io.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Clock Widget</title>

<style>
body {
    margin: 0;
    background: transparent;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

.clock-container {
    background: #111827;
    color: #f9fafb;
    padding: 30px 50px;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.25);
    text-align: center;
}

.time {
    font-size: 64px;
    font-weight: 600;
    letter-spacing: 2px;
}

.date {
    margin-top: 10px;
    font-size: 18px;
    opacity: 0.7;
}
</style>
</head>

<body>

<div class="clock-container">
    <div class="time" id="time">00:00:00</div>
    <div class="date" id="date">Loading...</div>
</div>

<script>
function updateClock() {
    const now = new Date();

    const time = now.toLocaleTimeString("pl-PL", {
        hour: "2-digit",
        minute: "2-digit",
        second: "2-digit"
    });

    const date = now.toLocaleDateString("pl-PL", {
        weekday: "long",
        year: "numeric",
        month: "long",
        day: "numeric"
    });

    document.getElementById("time").textContent = time;
    document.getElementById("date").textContent = date;
}

setInterval(updateClock, 1000);
updateClock();
</script>

</body>
</html>
