<div align="center">
  <h1>
    <span style="color:#00ff41; text-shadow: 0 0 15px #00ff41;">【</span>
    <span class="glitch" data-text="SEMTHA">SEMTHA</span>
    <span style="color:#00ff41; text-shadow: 0 0 15px #00ff41;">】</span>
  </h1>

  <h3>
    <span class="typing">> Initializing Software Engineer v2.3...</span>
  </h3>

  <p>
    <img src="https://komarev.com/ghpvc/?username=semitha&label=Systems%20Accessed&color=00ff41&style=for-the-badge" alt="views"/>
  </p>

  <br>

  <div class="terminal">
    <p><span class="prompt">$</span> whoami</p>
    <p><span class="output">Semitha — Software Engineer &amp; System Architect</span></p><br>
    
    <p><span class="prompt">$</span> current_mission</p>
    <p><span class="output">Building scalable applications • Breaking complex problems into clean code</span></p><br>
    
    <p><span class="prompt">$</span> skills --loaded</p>
    <p><span class="output">JavaScript • TypeScript • React • Next.js • Node.js • Python • Docker • AWS</span></p><br>
    
    <p><span class="prompt">$</span> status</p>
    <p><span class="output">ONLINE — Always learning • Always shipping</span></p>
  </div>

  <br>

  <h3>🛠️ TECH STACK</h3>
  <p>
    <img src="https://skillicons.dev/icons?i=javascript,typescript,react,nextjs,tailwind,nodejs,express,python,django,postgres,docker,aws,git&perline=8" />
  </p>

  <br><br>

  <h3>ACCESS TERMINAL</h3>
  
  <a href="https://linkedin.com/in/yourprofile" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-00ff41?style=for-the-badge&logo=linkedin&logoColor=black"/>
  </a>
  <a href="https://github.com/semitha" target="_blank">
    <img src="https://img.shields.io/badge/GITHUB-00ff41?style=for-the-badge&logo=github&logoColor=black"/>
  </a>
  <a href="mailto:your.email@gmail.com">
    <img src="https://img.shields.io/badge/EMAIL-00ff41?style=for-the-badge&logo=gmail&logoColor=black"/>
  </a>

</div>

<!-- ====================== STYLES & ANIMATIONS ====================== -->
<style>
  @import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
  
  body {
    background: #0a0a0a;
    color: #00ff41;
    font-family: 'VT323', monospace;
    overflow: hidden;
  }

  .glitch {
    font-size: 4.8rem;
    font-weight: bold;
    position: relative;
    color: #00ff41;
    animation: glitch 1.5s infinite;
  }

  .glitch:before,
  .glitch:after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  .glitch:before {
    left: 2px;
    text-shadow: -2px 0 #ff00ff;
    animation: glitch-anim 2s infinite linear alternate-reverse;
  }

  .glitch:after {
    left: -2px;
    text-shadow: -2px 0 #00ffff;
    animation: glitch-anim2 2.8s infinite linear alternate-reverse;
  }

  @keyframes glitch {
    0% { transform: translate(0); }
    20% { transform: translate(-2px, 2px); }
    40% { transform: translate(-2px, -2px); }
    60% { transform: translate(2px, 2px); }
    80% { transform: translate(2px, -2px); }
    100% { transform: translate(0); }
  }

  .typing {
    overflow: hidden;
    border-right: 3px solid #00ff41;
    white-space: nowrap;
    animation: typing 4s steps(35, end) forwards, blink .8s step-end infinite;
    font-size: 1.7rem;
    display: inline-block;
  }

  .terminal {
    background: rgba(10, 30, 10, 0.85);
    border: 2px solid #00ff41;
    padding: 25px;
    max-width: 720px;
    margin: 25px auto;
    text-align: left;
    box-shadow: 0 0 25px rgba(0, 255, 65, 0.4);
    font-size: 1.45rem;
    line-height: 1.6;
  }

  .prompt { color: #00ff9d; }
  .output { color: #aaffaa; }

  @keyframes typing {
    from { width: 0 }
    to { width: 100% }
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }
</style>

<!-- Matrix Rain Background -->
<canvas id="matrix" style="position:fixed; top:0; left:0; z-index:-1; opacity:0.18;"></canvas>

<script>
// Matrix Rain Effect
const canvas = document.getElementById('matrix');
const ctx = canvas.getContext('2d');

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const chars = "01アイウエオSEMTHAハッカーSOFTWAREENGINEERλΣΠ1234567890";
const fontSize = 15;
const columns = canvas.width / fontSize;
const drops = Array(Math.floor(columns)).fill(1);

function draw() {
  ctx.fillStyle = 'rgba(10, 20, 10, 0.07)';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = '#00ff41';
  ctx.font = fontSize + 'px monospace';

  for (let i = 0; i < drops.length; i++) {
    const text = chars[Math.floor(Math.random() * chars.length)];
    ctx.fillText(text, i * fontSize, drops[i] * fontSize);

    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
      drops[i] = 0;
    }
    drops[i]++;
  }
}

setInterval(draw, 35);

window.addEventListener('resize', () => {
  canvas.height = window.innerHeight;
  canvas.width = window.innerWidth;
});
</script>
