<div align="center">

<div id="clock-container" style="
background:#111827;
color:#f9fafb;
padding:30px 50px;
border-radius:20px;
box-shadow:0 10px 25px rgba(0,0,0,0.25);
font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;
display:inline-block;
text-align:center;
">

<div id="time" style="
font-size:64px;
font-weight:600;
letter-spacing:2px;
">
00:00
</div>

<div id="date" style="
margin-top:10px;
font-size:18px;
opacity:0.7;
">
Loading...
</div>

</div>

</div>

<script>
function updateClock() {
  const now = new Date();

  const time = now.toLocaleTimeString("pl-PL", {
    hour: "2-digit",
    minute: "2-digit"
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
