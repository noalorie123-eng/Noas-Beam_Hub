<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Noas Beam Hub</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap');

body {
    margin: 0;
    font-family: 'Orbitron', sans-serif;
    background: radial-gradient(circle at top, #2b0033, #0b0010);
    color: white;
}

header {
    text-align: center;
    padding: 50px 20px;
    background: linear-gradient(90deg, #ff2fa0, #ff5fd2);
    box-shadow: 0 0 30px #ff2fa0;
}

header h1 {
    font-size: 50px;
    text-shadow: 0 0 20px #ff2fa0;
}

header p {
    opacity: 0.8;
    font-size: 18px;
}

#search {
    display: block;
    margin: 20px auto;
    padding: 12px 20px;
    width: 300px;
    border-radius: 30px;
    border: none;
    font-size: 16px;
    outline: none;
}

.container {
    padding: 40px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.mod {
    background: rgba(255,255,255,0.05);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 0 25px rgba(255, 47, 160, 0.4);
    transition: transform 0.4s, box-shadow 0.4s;
}

.mod:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 40px rgba(255, 47, 160, 0.8);
}

.mod img {
    width: 100%;
    display: block;
}

.mod-content {
    padding: 20px;
}

.mod h2 {
    margin: 0 0 10px;
}

.mod p {
    font-size: 14px;
    opacity: 0.8;
}

.btn {
    display: inline-block;
    margin-top: 15px;
    padding: 12px 25px;
    border-radius: 30px;
    background: linear-gradient(90deg, #ff2fa0, #ff5fd2);
    color: black;
    text-decoration: none;
    font-weight: bold;
}

.btn:hover {
    filter: brightness(1.2);
}

footer {
    text-align: center;
    padding: 25px;
    font-size: 13px;
    opacity: 0.6;
}

/* Suchfunktion */
.hidden { display: none; }
</style>
</head>

<body>

<header>
    <h1>Noas Beam Hub</h1>
    <p>BeamNG.drive Mods – Neon • Fast Downloads</p>
    <input type="text" id="search" placeholder="Search Mods..." onkeyup="searchMods()">
</header>

<div class="container" id="mods-container">

<!-- Mod 1 -->
<div class="mod">
    <img src="https://via.placeholder.com/500x260">
    <div class="mod-content">
        <h2>BMW M4 G82</h2>
        <p>High quality visuals, realistic handling</p>
        <a class="btn" href="#" target="_blank">⬇ Download</a>
    </div>
</div>

<!-- Mod 2 -->
<div class="mod">
    <img src="https://via.placeholder.com/500x260">
    <div class="mod-content">
        <h2>Nissan GT-R R35</h2>
        <p>Drift & race setup included</p>
        <a class="btn" href="#" target="_blank">⬇ Download</a>
    </div>
</div>

<!-- Mod 3 -->
<div class="mod">
    <img src="https://via.placeholder.com/500x260">
    <div class="mod-content">
        <h2>Ford Mustang GT</h2>
        <p>Classic muscle car mod</p>
        <a class="btn" href="#" target="_blank">⬇ Download</a>
    </div>
</div>

</div>

<footer>
© 2026 Noas Beam Hub • Fan Made
</footer>

<script>
// Suchfunktion für Mods
function searchMods() {
    let input = document.getElementById('search').value.toLowerCase();
    let mods = document.getElementById('mods-container').getElementsByClassName('mod');

    for (let i = 0; i < mods.length; i++) {
        let title = mods[i].getElementsByTagName('h2')[0].innerText.toLowerCase();
        if (title.includes(input)) {
            mods[i].style.display = '';
        } else {
            mods[i].style.display = 'none';
        }
    }
}
</script>

</body>
</html>

