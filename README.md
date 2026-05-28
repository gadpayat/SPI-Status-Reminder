<!DOCTYPE html>
<html>
<head>
  <title>Reminder Prompt</title>

  <style>

    body{
      margin:0;
      font-family:Arial, sans-serif;
      background:transparent;
      overflow:hidden;
    }

    /* Slide down */
    @keyframes slideDown{
      from{transform:translateY(-120px);opacity:0;}
      to{transform:translateY(0);opacity:1;}
    }

    /* Blinking */
    @keyframes blink{
      0%{opacity:1;}
      50%{opacity:0.4;}
      100%{opacity:1;}
    }

    /* Train movement */
    @keyframes trainMove{
      0%{transform:translateX(0%);}
      100%{transform:translateX(-100%);}
    }

    /* Container */
    #container{
      width:100%;
      transition:opacity 2s ease;
    }

    /* Banner */
    #reminderBanner{
      width:100%;
      background:linear-gradient(to right,#ff8800,#ff0055);
      color:white;
      padding:18px 0;
      font-size:28px;
      font-weight:bold;
      text-align:center;

      animation: slideDown 1s ease, blink 1.2s infinite;
      overflow:hidden;
      white-space:nowrap;
    }

    /* Moving text */
    #movingText{
      display:inline-block;
      animation: trainMove 6s linear infinite;
      white-space:nowrap;
      padding-left:0%;
    }

  </style>
</head>

<body>

<div id="container">

  <div id="reminderBanner">
    <div id="movingText">
      ⏰ REMINDER: Updating of the Sub-Project Implementation Status (SPI) every Thursday, including reviewing progress, checking for issues or delays, and ensuring all sub-project statuses are current and accurate.
    </div>
  </div>

</div>

<script>

window.onload = () => {

  // Optional quick alert (can remove if not needed)
  alert("⏰ Reminder Activated!");

  // Auto remove after 15 seconds
  setTimeout(() => {

    const container =
    document.getElementById("container");

    container.style.opacity = "0";

    setTimeout(() => {
      container.style.display = "none";
    }, 2000);

  }, 15000);

};

</script>

</body>
</html># SPI-Status-Reminder
