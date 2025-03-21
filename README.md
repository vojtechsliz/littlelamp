<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vojtěch Sliž - Přepínač Témat</title>
<style>
  :root {
    --bg-color: #fdfdfd;
    --text-color: #333;
    --lamp-color: #ffcc00;
    --shadow-color: rgba(0, 0, 0, 0.15);
  }

  .dark-theme {
    --bg-color: #1e1e1e;
    --text-color: #e8e8e8;
    --lamp-color: #4fc3f7;
    --shadow-color: rgba(255, 255, 255, 0.2);
  }

  body {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    margin: 0;
    font-family: 'Roboto', Arial, sans-serif;
    background-color: var(--bg-color);
    color: var(--text-color);
    transition: background-color 0.5s ease, color 0.5s ease;
  }

  .button {
    font-size: 22px;
    padding: 12px 28px;
    border: 2px solid var(--text-color);
    background: none;
    color: var(--text-color);
    cursor: pointer;
    border-radius: 50px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: all 0.4s ease;
  }

  .button:hover {
    background-color: var(--text-color);
    color: var(--bg-color);
    transform: translateY(-2px);
  }

  .lamp {
    margin-top: 40px;
    width: 120px;
    height: 240px;
    background-color: var(--lamp-color);
    border-radius: 60px 60px 0 0;
    position: relative;
    box-shadow: 0 0 25px var(--lamp-color), 0 0 50px var(--lamp-color);
    transition: background-color 0.5s ease, box-shadow 0.5s ease;
  }

  .lamp-shadow {
    width: 140px;
    height: 30px;
    background-color: var(--shadow-color);
    border-radius: 50%;
    margin-top: 20px;
    transition: background-color 0.5s ease;
    filter: blur(4px);
  }
</style>
</head>
<body>

<button class="button" onclick="toggleTheme()">Vojtěch Sliž</button>

<div class="lamp"></div>
<div class="lamp-shadow"></div>

<script>
  function toggleTheme() {
    document.body.classList.toggle('dark-theme');
  }
</script>

</body>
</html>
