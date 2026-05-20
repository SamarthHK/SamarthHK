<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Samarth | GitHub Profile</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #09090f;
      --card: rgba(18, 18, 28, 0.8);
      --border: rgba(255,255,255,0.08);
      --primary: #8b5cf6;
      --secondary: #22d3ee;
      --text: #f4f4f5;
      --muted: #a1a1aa;
      --glow: 0 0 25px rgba(139,92,246,0.4);
    }

    body {
      background: radial-gradient(circle at top left, rgba(139,92,246,0.25), transparent 30%),
                  radial-gradient(circle at bottom right, rgba(34,211,238,0.18), transparent 25%),
                  var(--bg);
      color: var(--text);
      font-family: 'Space Grotesk', sans-serif;
      overflow-x: hidden;
      min-height: 100vh;
      padding: 40px 20px;
    }

    .container {
      max-width: 1200px;
      margin: auto;
    }

    .hero {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 40px;
      align-items: center;
      margin-bottom: 40px;
    }

    .hero-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 28px;
      padding: 40px;
      backdrop-filter: blur(12px);
      box-shadow: var(--glow);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      width: 220px;
      height: 220px;
      background: rgba(139,92,246,0.18);
      border-radius: 50%;
      top: -100px;
      right: -100px;
      filter: blur(40px);
    }

    h1 {
      font-size: 4rem;
      margin-bottom: 10px;
      line-height: 1;
    }

    .gradient {
      background: linear-gradient(90deg, #8b5cf6, #22d3ee);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .subtitle {
      color: var(--muted);
      font-size: 1.1rem;
      margin-bottom: 24px;
      line-height: 1.6;
    }

    .tag-container {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 18px;
    }

    .tag {
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.08);
      padding: 10px 16px;
      border-radius: 999px;
      color: #e4e4e7;
      font-size: 0.92rem;
      transition: 0.3s;
    }

    .tag:hover {
      transform: translateY(-3px);
      background: rgba(139,92,246,0.15);
    }

    .profile-image {
      height: 100%;
      min-height: 350px;
      border-radius: 28px;
      background: linear-gradient(145deg, rgba(139,92,246,0.2), rgba(34,211,238,0.12));
      border: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
    }

    .profile-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      position: absolute;
      inset: 0;
    }

    .placeholder {
      z-index: 2;
      color: rgba(255,255,255,0.45);
      text-align: center;
      padding: 20px;
      font-size: 1rem;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 24px;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 24px;
      padding: 28px;
      backdrop-filter: blur(10px);
      transition: 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .card:hover {
      transform: translateY(-8px);
      border-color: rgba(139,92,246,0.45);
      box-shadow: 0 15px 40px rgba(0,0,0,0.35);
    }

    .card h2 {
      margin-bottom: 18px;
      font-size: 1.4rem;
    }

    .card p, .card li {
      color: var(--muted);
      line-height: 1.8;
    }

    ul {
      list-style: none;
    }

    li::before {
      content: "✦";
      color: var(--secondary);
      margin-right: 10px;
    }

    .anime-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 16px;
      margin-top: 18px;
    }

    .anime-card {
      background: rgba(255,255,255,0.04);
      border-radius: 18px;
      overflow: hidden;
      border: 1px solid rgba(255,255,255,0.06);
      transition: 0.3s;
    }

    .anime-card:hover {
      transform: scale(1.03);
    }

    .anime-image {
      height: 150px;
      background: rgba(255,255,255,0.03);
      display: flex;
      align-items: center;
      justify-content: center;
      color: rgba(255,255,255,0.35);
      font-size: 0.9rem;
      position: relative;
      overflow: hidden;
    }

    .anime-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      position: absolute;
      inset: 0;
    }

    .anime-title {
      padding: 14px;
      font-size: 0.95rem;
      text-align: center;
      color: #f4f4f5;
    }

    .project-highlight {
      margin-top: 16px;
      padding: 18px;
      border-radius: 18px;
      background: rgba(139,92,246,0.08);
      border: 1px solid rgba(139,92,246,0.2);
    }

    .footer {
      margin-top: 50px;
      text-align: center;
      color: rgba(255,255,255,0.45);
      font-size: 0.95rem;
    }

    .cursor {
      color: var(--secondary);
      animation: blink 1s infinite;
    }

    @keyframes blink {
      50% {
        opacity: 0;
      }
    }

    @media (max-width: 900px) {
      .hero {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: 3rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">

    <section class="hero">
      <div class="hero-card">
        <h1>
          Hi, I'm <span class="gradient">Samarth</span><span class="cursor">_</span>
        </h1>

        <p class="subtitle">
          15 year old developer from Washington State 🇺🇸<br>
          Freshman at Cavelero Mid High • 6'2 btw 😭<br><br>
          Currently obsessed with backend engineering, networking, and understanding how the web actually works under the hood.
        </p>

        <div class="tag-container">
          <div class="tag">Java</div>
          <div class="tag">Backend</div>
          <div class="tag">HTTP</div>
          <div class="tag">Networking</div>
          <div class="tag">System Architecture</div>
          <div class="tag">Databases</div>
          <div class="tag">Neural Networks</div>
          <div class="tag">Indian 🇮🇳</div>
        </div>
      </div>

      <div class="profile-image">
        <!-- Replace with your own image -->
        <!-- <img src="images/profile.png" alt="Profile"> -->
        <div class="placeholder">
          Drop your profile image here<br>
          <small>Replace the commented img tag</small>
        </div>
      </div>
    </section>

    <section class="grid">

      <div class="card">
        <h2>🚀 Current Project</h2>
        <p>
          Working on <strong>Tabris</strong> (named after Kaworu from Evangelion) — my own custom HTTP server built from raw sockets.
        </p>

        <div class="project-highlight">
          <p>
            Building the backend for <strong>RemixxerArt</strong> while learning backend engineering deeply before moving into Spring Boot.
          </p>
        </div>
      </div>

      <div class="card">
        <h2>🧠 Interests</h2>
        <ul>
          <li>Backend Engineering</li>
          <li>Networking</li>
          <li>System Architecture</li>
          <li>Databases</li>
          <li>Neural Networks</li>
        </ul>
      </div>

      <div class="card">
        <h2>⚒️ Tech Stack</h2>
        <div class="tag-container">
          <div class="tag">Java</div>
          <div class="tag">Python</div>
          <div class="tag">SQL</div>
        </div>
      </div>

      <div class="card">
        <h2>📚 Currently Learning</h2>
        <ul>
          <li>Java Core</li>
          <li>Networking</li>
          <li>HTTP Internals</li>
          <li>Backend Development</li>
        </ul>
      </div>

      <div class="card">
        <h2>🎯 Goals</h2>
        <p>
          Create RemixxerArt by the end of the year and become confident with:
        </p>

        <div class="tag-container" style="margin-top: 18px;">
          <div class="tag">Spring</div>
          <div class="tag">Linux</div>
          <div class="tag">Backend</div>
        </div>
      </div>

      <div class="card">
        <h2>🌙 Favorite Anime</h2>

        <div class="anime-grid">
          <div class="anime-card">
            <div class="anime-image">
              <!-- <img src="images/eva.jpg"> -->
              Evangelion Image
            </div>
            <div class="anime-title">Evangelion</div>
          </div>

          <div class="anime-card">
            <div class="anime-image">
              <!-- <img src="images/deathparade.jpg"> -->
              Death Parade Image
            </div>
            <div class="anime-title">Death Parade</div>
          </div>

          <div class="anime-card">
            <div class="anime-image">
              <!-- <img src="images/lain.jpg"> -->
              Lain Image
            </div>
            <div class="anime-title">Serial Experiments Lain</div>
          </div>

          <div class="anime-card">
            <div class="anime-image">
              <!-- <img src="images/callofthenight.jpg"> -->
              Call of the Night Image
            </div>
            <div class="anime-title">Call of the Night</div>
          </div>

          <div class="anime-card">
            <div class="anime-image">
              <!-- <img src="images/oshinoko.jpg"> -->
              Oshi No Ko Image
            </div>
            <div class="anime-title">Oshi No Ko</div>
          </div>
        </div>
      </div>

    </section>

    <div class="footer">
      <p>
        “Understanding things from the ground up.”
      </p>
    </div>
  </div>

  <script>
    const cards = document.querySelectorAll('.card');

    cards.forEach((card, index) => {
      card.style.opacity = '0';
      card.style.transform = 'translateY(20px)';

      setTimeout(() => {
        card.style.transition = '0.6s ease';
        card.style.opacity = '1';
        card.style.transform = 'translateY(0px)';
      }, index * 120);
    });
  </script>
</body>
</html>
