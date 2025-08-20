<?xml version="1.0" encoding="UTF-8"?>
<!-- Banner Animado SVG para GitHub Profile -->
<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="300" viewBox="0 0 1200 300">
  <defs>
    <linearGradient id="grad" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0f172a"/>
      <stop offset="100%" stop-color="#1e293b"/>
    </linearGradient>
    <filter id="glow" x="-50%" y="-50%" width="200%" height="200%">
      <feDropShadow dx="0" dy="0" stdDeviation="3" flood-color="#38bdf8"/>
    </filter>
    <mask id="typing-mask">
      <rect id="typing-rect" x="0" y="0" width="0" height="100%" fill="#fff"/>
    </mask>
  </defs>

  <style><![CDATA[
    .bg { fill: url(#grad); }
    .title { font: bold 48px monospace; fill: #e2e8f0; }
    .subtitle { font: 20px monospace; fill: #94a3b8; }
    .cursor { fill: #38bdf8; }

    @keyframes typing { from { width: 0; } to { width: 800px; } }
    @keyframes blink { 0%, 50% { opacity: 1; } 51%, 100% { opacity: 0; } }
    #typing-rect { animation: typing 4s steps(40,end) forwards; }
    .cursor { animation: blink 1s infinite; }

    @keyframes float { 0%,100% { transform: translateY(0); } 50% { transform: translateY(-8px); } }
    .icon { filter: url(#glow); animation: float 4s ease-in-out infinite; }
  ]]></style>

  <rect class="bg" width="1200" height="300"/>

  <!-- Texto com efeito de digitação -->
  <g transform="translate(100,150)">
    <text class="title" mask="url(#typing-mask)">Olá, eu sou o Gustavo 👨‍💻</text>
    <rect class="cursor" x="805" y="-40" width="10" height="50"/>
  </g>

  <text class="subtitle" x="100" y="200">Desenvolvedor Front-End | HTML • CSS • JavaScript</text>

  <!-- Ícones flutuando -->
  <g class="icon" transform="translate(1050,100)">
    <circle r="25" fill="#38bdf8"/>
    <text x="-15" y="10" font-size="24" fill="#0f172a">{ }</text>
  </g>
  <g class="icon" transform="translate(950,220)">
    <circle r="25" fill="#facc15"/>
    <text x="-12" y="10" font-size="24" fill="#0f172a">&lt;/&gt;</text>
  </g>
</svg>


<h1 align="center">👋 Olá, mundo! Eu sou <strong>Gustavo de Lima Maximo</strong> 🌍</h1>

<p align="center">
  💻 Estudante de Programação | Futuro Desenvolvedor Full Stack <br>
  🚀 Transformando ideias em soluções através do código
</p>

---

##  Sobre mim
- 📍 São Paulo - SP, Brasil  
- 🧑‍💻 Pronome: Ele/dele  
- 🎯 Objetivo: Tornar-me um desenvolvedor Full Stack completo  
- 📚 Apaixonado por aprender novas tecnologias e boas práticas  
- 🌱 Filosofia: *"O começo é difícil, o meio é doloroso, mas no final te torna alguém melhor do que ontem"*  

---
Tecnologias e ferramentas 

### 🎨 Front-end  
<p>
  <img src="https://skillicons.dev/icons?i=html" width="45" alt="HTML5"> 
  <b>HTML5</b> — Estrutura a base de qualquer página web
</p>
<p>
  <img src="https://skillicons.dev/icons?i=css" width="45" alt="CSS3"> 
  <b>CSS3</b> — Cria estilos modernos e responsivos
</p>
<p>
  <img src="https://skillicons.dev/icons?i=js" width="45" alt="JavaScript"> 
  <b>JavaScript</b> — Dá vida e interatividade às aplicações
</p>
<p>
  <img src="https://skillicons.dev/icons?i=react" width="45" alt="React"> 
  <b>React.js</b> — Framework para interfaces dinâmicas
</p>

### 🖥️ Back-end  
<p>
  <img src="https://skillicons.dev/icons?i=nodejs" width="45" alt="Node.js"> 
  <b>Node.js</b> — Criação de servidores rápidos e escaláveis
</p>

### 🗄️ Banco de Dados  
<p>
  <img src="https://skillicons.dev/icons?i=mysql" width="45" alt="MySQL"> 
  <b>MySQL</b> — Banco de dados relacional para armazenar informações
</p>


---

## 📊 Estatísticas do GitHub
<div align="center">
  
  ![GitHub Stats](https://github-readme-stats.vercel.app/api?username=gustavolmx&show_icons=true&theme=transparent&hide_border=true&title_color=ffffff&text_color=ffffff&icon_color=808080)
  
  ![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=gustavolmx&layout=compact&theme=transparent&hide_border=true&title_color=ffffff&text_color=ffffff)

</div>


## 🌐 Onde me encontrar
<p align="left">
  <a href="https://www.linkedin.com/in/gustavo-de-lima-máximo-19635 2317" target="_blank">
    <img src="https://skillicons.dev/icons?i=linkedin" width="50" alt="LinkedIn">
  </a>
  <a href="mailto:maximogustavo47@gmail.com">
    <img src="https://skillicons.dev/icons?i=gmail" width="50" alt="E-mail">
  </a>
</p