<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NEO-SEKAI//SYNC 2025</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">
<style>
/* Global Styles */
body {
  margin: 0;
  font-family: 'Roboto', sans-serif;
  background: #0a0a0a;
  color: #fff;
  overflow-x: hidden;
  scroll-behavior: smooth;
}

h1, h2, h3 { font-family: 'Orbitron', sans-serif; }
a { color: inherit; text-decoration: none; }
ul { list-style: none; padding: 0; }

/* Neon Scrolling Background */
body::before {
  content: "";
  position: fixed;
  top:0; left:0; width:100%; height:100%;
  background: linear-gradient(90deg, #6a00ff, #00e0ff, #ff00ff);
  background-size: 300% 300%;
  animation: gradientMove 20s ease infinite;
  z-index: -1;
  opacity: 0.05;
}
@keyframes gradientMove {
  0% {background-position:0% 50%;}
  50% {background-position:100% 50%;}
  100% {background-position:0% 50%;}
}

/* Header */
header {
  background: rgba(0,0,0,0.85);
  padding: 1rem 2rem;
  text-align: center;
  position: sticky;
  top: 0;
  z-index: 100;
}
header h1 {
  font-size: 2.5rem;
  text-shadow: 0 0 20px #00e0ff;
}
nav a {
  margin: 0 1rem;
  font-weight: 500;
  transition: color 0.3s;
}
nav a:hover { color: #ffea00; }

/* Sections */
section {
  padding: 4rem 2rem;
  max-width: 1200px;
  margin: auto;
}
section h2 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #ffea00;
  text-shadow: 0 0 10px #ffea00;
}

/* Acts Grid */
.acts {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}
.act-card {
  background: rgba(10,10,10,0.9);
  border-radius: 15px;
  padding: 1.5rem;
  text-align: center;
  transform: translateY(50px);
  opacity: 0;
  transition: transform 0.6s, opacity 0.6s, box-shadow 0.3s;
  border: 1px solid #333;
  cursor: pointer;
}
.act-card.visible {
  transform: translateY(0);
  opacity: 1;
  box-shadow: 0 0 20px #00e0ff;
}
.act-card h3 { margin-bottom: 1rem; color: #00e0ff; }
.song-list li {
  padding: 0.3rem 0;
  font-size: 0.95rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.play-btn {
  background: #00e0ff;
  border: none;
  color: #000;
  padding: 0.2rem 0.6rem;
  border-radius: 5px;
  cursor: pointer;
  font-size: 0.8rem;
  margin-left: 0.5rem;
  transition: 0.3s;
}
.play-btn:hover { background: #ffea00; }

/* Members Section */
.members {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 2rem;
}
.member-card {
  background: rgba(10,10,10,0.9);
  border-radius: 15px;
  padding: 1rem;
  text-align: center;
  border: 1px solid #333;
  box-shadow: 0 0 5px #ff00ff;
  transition: transform 0.5s, box-shadow 0.5s;
}
.member-card:hover {
  transform: translateY(-10px) rotateY(10deg);
  box-shadow: 0 0 25px #ff00ff;
}
.member-card h3 { color: #ff00ff; margin-bottom: 0.5rem; }
.member-card p { font-size: 0.9rem; line-height: 1.4; }

/* Footer */
footer {
  text-align: center;
  padding: 2rem;
  background: #111;
  border-top: 1px solid #333;
  color: #777;
}
</style>
</head>
<body>

<header>
  <h1>NEO-SEKAI//SYNC 2025</h1>
  <nav>
    <a href="#acts">Acts</a>
    <a href="#members">Members</a>
    <a href="#live">Live Collabs</a>
  </nav>
</header>

<!-- Acts Section -->
<section id="acts">
<h2>Acts & Songlists</h2>
<div class="acts">
  <!-- ACT I -->
  <div class="act-card">
    <h3>ACT I — DIGITAL AWAKENING (Daft Punk)</h3>
    <ul class="song-list">
      <li>One More Time <button class="play-btn" onclick="playSong('audio1')">▶</button></li>
      <li>Harder, Better, Faster, Stronger <button class="play-btn" onclick="playSong('audio2')">▶</button></li>
      <li>Digital Love <button class="play-btn" onclick="playSong('audio3')">▶</button></li>
      <li>Crescendolls <button class="play-btn" onclick="playSong('audio4')">▶</button></li>
      <li>Derezzed <button class="play-btn" onclick="playSong('audio5')">▶</button></li>
      <li>Instant Crush <button class="play-btn" onclick="playSong('audio6')">▶</button></li>
      <li>High Life <button class="play-btn" onclick="playSong('audio7')">▶</button></li>
    </ul>
  </div>

  <!-- ACT II -->
  <div class="act-card">
    <h3>ACT II — NEON DREAMS (Galantis)</h3>
    <ul class="song-list">
      <li>Runaway (U & I) <button class="play-btn" onclick="playSong('audio8')">▶</button></li>
      <li>No Money <button class="play-btn" onclick="playSong('audio9')">▶</button></li>
      <li>Peanut Butter Jelly <button class="play-btn" onclick="playSong('audio10')">▶</button></li>
      <li>Bang Bang! <button class="play-btn" onclick="playSong('audio11')">▶</button></li>
    </ul>
  </div>

  <!-- ACT III -->
  <div class="act-card">
    <h3>ACT III — LUMINESCENCE (Deadmau5)</h3>
    <ul class="song-list">
      <li>Ghosts ’n Stuff <button class="play-btn" onclick="playSong('audio12')">▶</button></li>
      <li>Strobe <button class="play-btn" onclick="playSong('audio13')">▶</button></li>
      <li>Raise Your Weapon <button class="play-btn" onclick="playSong('audio14')">▶</button></li>
      <li>Monophobia <button class="play-btn" onclick="playSong('audio15')">▶</button></li>
    </ul>
  </div>

  <!-- ACT IV -->
  <div class="act-card">
    <h3>ACT IV — SYNTH REBIRTH (Alan Walker)</h3>
    <ul class="song-list">
      <li>Faded <button class="play-btn" onclick="playSong('audio16')">▶</button></li>
      <li>Alone <button class="play-btn" onclick="playSong('audio17')">▶</button></li>
      <li>The Spectre <button class="play-btn" onclick="playSong('audio18')">▶</button></li>
      <li>Better Off (Alone Pt.3) <button class="play-btn" onclick="playSong('audio19')">▶</button></li>
    </ul>
  </div>

  <!-- ACT V -->
  <div class="act-card">
    <h3>ACT V — URBAN SYNC (Vivid BAD SQUAD × Nightcord)</h3>
    <ul class="song-list">
      <li>Ready Steady <button class="play-btn" onclick="playSong('audio20')">▶</button></li>
      <li>Flyer <button class="play-btn" onclick="playSong('audio21')">▶</button></li>
      <li>Ultra C <button class="play-btn" onclick="playSong('audio22')">▶</button></li>
      <li>Beyond the Way <button class="play-btn" onclick="playSong('audio23')">▶</button></li>
      <li>Twilight Light <button class="play-btn" onclick="playSong('audio24')">▶</button></li>
      <li>Ready Steady × Ultra C [Final Remix] <button class="play-btn" onclick="playSong('audio25')">▶</button></li>
    </ul>
  </div>

  <!-- ACT VI -->
  <div class="act-card">
    <h3>ACT VI — VOCALOID SEKAI (Miku & Friends)</h3>
    <ul class="song-list">
      <li>Flyer <button class="play-btn" onclick="playSong('audio26')">▶</button></li>
      <li>Ready Steady <button class="play-btn" onclick="playSong('audio27')">▶</button></li>
      <li>Tell Your World <button class="play-btn" onclick="playSong('audio28')">▶</button></li>
      <li>Ultra C (Vivid BAD SQUAD Ver) <button class="play-btn" onclick="playSong('audio29')">▶</button></li>
      <li>Virtual Connection Remix <button class="play-btn" onclick="playSong('audio30')">▶</button></li>
    </ul>
  </div>

  <!-- ACT VII -->
  <div class="act-card">
    <h3>ACT VII — PARALLEL BEAT (Gorillaz)</h3>
    <ul class="song-list">
      <li>Clint Eastwood <button class="play-btn" onclick="playSong('audio31')">▶</button></li>
      <li>Feel Good Inc <button class="play-btn" onclick="playSong('audio32')">▶</button></li>
      <li>DARE <button class="play-btn" onclick="playSong('audio33')">▶</button></li>
      <li>Cracker Island <button class="play-btn" onclick="playSong('audio34')">▶</button></li>
    </ul>
  </div>

  <!-- ACT VIII -->
  <div class="act-card">
    <h3>ACT VIII — THE SYNC FUSION (Finale)</h3>
    <ul class="song-list">
      <li>NEO-SEKAI//SYNC Finale Theme <button class="play-btn" onclick="playSong('audio35')">▶</button></li>
    </ul>
  </div>
</div>
</section>

<!-- Members Section -->
<section id="members">
<h2>Official Members</h2>
<div class="members">
  <div class="member-card">
    <h3>The Architects</h3>
    <p>Daft Punk – Thomas Bangalter & Guy-Manuel<br>
    French house × cinematic synths × digital legacy<br>
    "They built the bridge between analog dreams and digital souls."</p>
  </div>
  <div class="member-card">
    <h3>The Virtual Engineers</h3>
    <p>Deadmau5 & Galantis<br>
    EDM rhythm & euphoric festival drops<br>
    "The Pulse of the Network"</p>
  </div>
  <div class="member-card">
    <h3>The Visionaries</h3>
    <p>Gorillaz (2D, Murdoc, Noodle, Russel)<br>
    Alt electronica × hip-hop × surreal pop<br>
    "Hybrid bridge between human groove & animated energy"</p>
  </div>
  <div class="member-card">
    <h3>The Virtual Divas</h3>
    <p>Hatsune Miku & Vocaloids<br>
    Digital pop voices / emotional heart of the sync</p>
  </div>
  <div class="member-card">
    <h3>The Street Dreamers</h3>
    <p>Vivid BAD SQUAD<br>
    J-pop × EDM × hip-hop × future bass<br>
    Neo-Tokyo’s underground rising to the main stage</p>
  </div>
</div>
</section>

<!-- Live Collaborators -->
<section id="live">
<h2>Live Collaborators</h2>
<ul class="song-list" style="text-align:center;">
  <li>Porter Robinson & Madeon – Dreamscape sound designers</li>
  <li>Hiroyuki Sawano – Cinematic composer</li>
  <li>Rei (VBS) – Live holographic DJ</li>
  <li>Pharrell Williams – Soul/funk infusion</li>
</ul>
</section>

<footer>
  &copy; 2025 NEO-SEKAI//SYNC | All Rights Reserved
</footer>

<!-- Audio Elements -->
<script>
for(let i=1;i<=35;i++){
  let audio = document.createElement("audio");
  audio.id = "audio"+i;
  audio.src = "audio/song"+i+".mp3"; // Replace with real audio files
  document.body.appendChild(audio);
}

function playSong(id){
  const audio = document.getElementById(id);
  if(audio.paused){
    audio.play();
  } else {
    audio.pause();
    audio.currentTime = 0;
  }
}

// Scroll Reveal Animation
const actCards = document.querySelectorAll('.act-card');
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add('visible');
    }
  });
}, {threshold:0.3});
actCards.forEach(card => observer.observe(card));
</script>

</body>
</html>
neo-sekai-sync/
├── index.html
├── audio/
│   ├── song1.mp3
│   ├── song2.mp3
│   ├── ...
│   └── song35.mp3
├── css/
│   └── style.css      (optional: if you move CSS out of HTML)
├── img/
│   └── favicon.png    (optional)
└── README.md          (optional, for GitHub repo info)

