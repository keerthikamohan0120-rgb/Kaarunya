<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Ear priecing Invitation</title>
  <link href="https://fonts.googleapis.com/css?family=Dancing+Script|Arvo" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <style>
    body { font-family: 'Dancing Script', cursive; background: linear-gradient(to bottom, #f9e4e4, #d4a5a5); text-align: center; margin: 0; padding: 20px; }
    .title h1 { font-size: 4em; color: #8b0000; margin: 0; }
    .title h2 { font-size: 5em; color: gold; }
    .title h3 { font-size: 2em; color: #333; }
    .date, .place { color: #8b0000; font-weight: bold; }
    #time { font-size: 3em; margin: 20px 0; }
    .actions a { display: inline-block; margin: 10px; padding: 15px 30px; background: gold; color: #8b0000; text-decoration: none; border-radius: 25px; }
    .footer { font-size: 1.2em; color: #666; }
    @media (max-width: 768px) { .title h1 { font-size: 2.5em; } .title h2 { font-size: 3.5em; } }
  </style>
</head>
<body>
  <div class="title">
    <h1>Bride Name</h1>
    <h2>&</h2>
    <h1>Groom Name</h1>
    <h3>Are getting married</h3>
    <p>on <span class="date">April 20, 2026</span><br>At <span class="place">Venue Name, Chennai</span></p>
  </div>
  <div id="time">Countdown Timer Here</div>
  <div class="actions">
    <a href="https://maps.google.com/yourvenue" target="_blank">See Venue</a>
    <a href="rsvp-form-link">RSVP</a>
  </div>
  <p class="footer">Join us in our joy! Contact: +91-XXXXXXX</p>
  
  <script>
    // Simple countdown example (customize date)
    const weddingDate = new Date('April 20, 2026 18:00:00').getTime();
    const timer = setInterval(() => {
      const now = new Date().getTime();
      const distance = weddingDate - now;
      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      document.getElementById('time').innerHTML = days + 'd ' + hours + 'h remaining';
      if (distance < 0) { clearInterval(timer); document.getElementById('time').innerHTML = 'We are married!'; }
    }, 1000);
  </script>
</body>
</html>
