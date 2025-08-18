<!-- Salve como: assets/banner-github.svg e use no README:
<p align="center"><img src="assets/banner-github.svg" width="100%" alt="Banner animado de programação"></p>
-->
<svg width="1200" height="360" viewBox="0 0 1200 360" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Fundo gradiente escuro -->
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#000000"/>
      <stop offset="100%" stop-color="#0b0b0f"/>
    </linearGradient>

    <!-- Efeito glow neon -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Gradiente neon -->
    <linearGradient id="neon" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#00e5ff"/>
      <stop offset="100%" stop-color="#00ff95"/>
    </linearGradient>

    <!-- Cursor piscando -->
    <style>
      @keyframes blink { 50% { opacity: 0; } }
      @keyframes float1 { 0% { transform: translateY(0px); } 50% { transform: translateY(-6px);} 100% { transform: translateY(0px);} }
      @keyframes float2 { 0% { transform: translateY(0px); } 50% { transform: translateY(6px);} 100% { transform: translateY(0px);} }
      @keyframes dash {
        0% { stroke-dashoffset: 1000; }
        100% { stroke-dashoffset: 0; }
      }
      .cursor { animation: blink 1s step-end infinite; }
      .float1 { animation: float1 4s ease-in-out infinite; }
      .float2 { animation: float2 5s ease-in-out infinite; }
      .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, "Liberation Mono", monospace; }
      .sans { font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, "Helvetica Neue", Arial, "Noto Sans", sans-serif; }
    </style>

    <!-- Símbolo para “código caindo” -->
    <symbol id="codeLine" viewBox="0 0 4 40">
      <rect x="1.6" y="0" width="0.8" height="40" fill="url(#neon)"/>
    </symbol>
  </defs>

  <!-- Fundo -->
  <rect width="1200" height="360" fill="url(#bg)"/>

  <!-- Linhas diagonais decorativas com traço animado -->
  <g opacity="0.2">
    <path d="M-100 320 L1300 -60" stroke="url(#neon)" stroke-width="2" stroke-linecap="round"
          stroke-dasharray="8 10">
      <animate attributeName="stroke-dashoffset" from="0" to="-200" dur="8s" repeatCount="indefinite"/>
    </path>
    <path d="M-120 380 L1320 0" stroke="url(#neon)" stroke-width="2" stroke-linecap="round"
          stroke-dasharray="6 12">
      <animate attributeName="stroke-dashoffset" from="0" to="200" dur="10s" repeatCount="indefinite"/>
    </path>
  </g>

  <!-- Chuva de código suave (colunas) -->
  <g opacity="0.15" filter="url(#glow)">
    <use href="#codeLine" x="80">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="6s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="180">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="5s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="260">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="7s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="380">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="6.5s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="520">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="5.5s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="680">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="7.2s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="820">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="6.2s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="950">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="5.8s" repeatCount="indefinite"/>
    </use>
    <use href="#codeLine" x="1080">
      <animateTransform attributeName="transform" type="translate" from="0 -360" to="0 360" dur="6.8s" repeatCount="indefinite"/>
    </use>
  </g>

  <!-- Título com neon -->
  <g filter="url(#glow)">
    <text x="600" y="130" text-anchor="middle" class="sans" font-size="40" fill="url(#neon)" letter-spacing="1.5">
      Gustavo de Lima Maximo
    </text>
    <text x="600" y="168" text-anchor="middle" class="sans" font-size="20" fill="#cfcfcf">
      Estudante de Programação • Futuro Dev Full Stack
    </text>
  </g>

  <!-- Linha animada sob o título -->
  <line x1="360" y1="185" x2="840" y2="185" stroke="url(#neon)" stroke-width="2" stroke-linecap="round"
        stroke-dasharray="1000" stroke-dashoffset="1000" filter="url(#glow)">
    <animate attributeName="stroke-dashoffset" from="1000" to="0" dur="2.8s" fill="freeze"/>
  </line>

  <!-- Texto “codando” com cursor -->
  <g class="mono" transform="translate(0,10)">
    <text x="600" y="225" text-anchor="middle" font-size="18" fill="#e6e6e6">&lt;code&gt; Transformando ideias em soluções &lt;/code&gt;</text>
    <rect x="874" y="208" width="12" height="22" fill="#ffffff" class="cursor"/>
  </g>

  <!-- Ícones minimalistas das stacks (círculos com orbit) -->
  <!-- Órbita 1 -->
  <g transform="translate(600,250)">
    <circle r="78" fill="none" stroke="#1f1f24" stroke-width="1"/>
    <g filter="url(#glow)">
      <g>
        <circle cx="78" cy="0" r="16" fill="url(#neon)"/>
        <text x="78" y="5" text-anchor="middle" font-size="10" class="mono" fill="#0b0b0b">HTML</text>
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="12s" repeatCount="indefinite"/>
      </g>
      <g>
        <circle cx="-78" cy="0" r="16" fill="url(#neon)"/>
        <text x="-78" y="5" text-anchor="middle" font-size="10" class="mono" fill="#0b0b0b">CSS</text>
        <animateTransform attributeName="transform" type="rotate" from="180" to="540" dur="12s" repeatCount="indefinite"/>
      </g>
    </g>
  </g>

  <!-- Órbita 2 -->
  <g transform="translate(600,250)">
    <circle r="118" fill="none" stroke="#1f1f24" stroke-width="1"/>
    <g filter="url(#glow)">
      <g>
        <circle cx="118" cy="0" r="16" fill="url(#neon)"/>
        <text x="118" y="5" text-anchor="middle" font-size="10" class="mono" fill="#0b0b0b">JS</text>
        <animateTransform attributeName="transform" type="rotate" from="0" to="-360" dur="16s" repeatCount="indefinite"/>
      </g>
      <g>
        <circle cx="-118" cy="0" r="16" fill="url(#neon)"/>
        <text x="-118" y="5" text-anchor="middle" font-size="10" class="mono" fill="#0b0b0b">React</text>
        <animateTransform attributeName="transform" type="rotate" from="180" to="-180" dur="16s" repeatCount="indefinite"/>
      </g>
    </g>
  </g>

  <!-- Órbita 3 -->
  <g transform="translate(600,250)">
    <circle r="154" fill="none" stroke="#1f1f24" stroke-width="1"/>
    <g filter="url(#glow)">
      <g>
        <circle cx="154" cy="0" r="16" fill="url(#neon)"/>
        <text x="154" y="5" text-anchor="middle" font-size="10" class="mono" fill="#0b0b0b">Node</text>
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="20s" repeatCount="indefinite"/>
      </g>
      <g>
        <circle cx="-154" cy="0" r="16" fill="url(#neon)"/>
        <text x="-154" y="5" text-anchor="middle" font-size="10" class="mono" fill="#0b0b0b">MySQL</text>
        <animateTransform attributeName="transform" type="rotate" from="180" to="540" dur="20s" repeatCount="indefinite"/>
      </g>
    </g>
  </g>

  <!-- Rodapé discreto -->
  <text x="600" y="335" text-anchor="middle" class="mono" font-size="12" fill="#888">
    #black • #neon • #programação
  </text>
</svg>

<h1 align="center">👋 Olá, mundo! Eu sou <strong>Gustavo de Lima Maximo</strong> 🌍</h1>

<p align="center">
  💻 Estudante de Programação | Futuro Desenvolvedor Full Stack <br>
  🚀 Transformando ideias em soluções através do código
</p>

---

##  Sobre mim
-  São Paulo - SP, Brasil  
-  Pronome: Ele/dele  
- 🎯 Objetivo: Tornar-me um desenvolvedor Full Stack completo  
- 📚 Apaixonado por aprender novas tecnologias e boas práticas  
- 🌱 Filosofia: *"O começo é difícil, o meio é doloroso, mas no final te torna alguém melhor do que ontem"*  

---

## ⚡ Tecnologias e Ferramentas

<p align="center">
  <img src="https://raw.githubusercontent.com/gustavolmx/gustavolmx/main/assets/dev-coding.gif" width="600" alt="Programador animado">
</p>

### 🎨 Front-end  
<div align="center">

| Logo | Descrição |
|------|-----------|
| <img src="https://skillicons.dev/icons?i=html" width="45" alt="HTML5"> | **HTML5** → Estrutura a base de qualquer página web |
| <img src="https://skillicons.dev/icons?i=css" width="45" alt="CSS3"> | **CSS3** → Cria estilos modernos, responsivos e elegantes |
| <img src="https://skillicons.dev/icons?i=js" width="45" alt="JavaScript"> | **JavaScript** → Dá vida e interatividade às aplicações |
| <img src="https://skillicons.dev/icons?i=react" width="45" alt="React"> | **React.js** → Framework para interfaces rápidas e dinâmicas |

</div>

### 🖥️ Back-end  
<div align="center">

| Logo | Descrição |
|------|-----------|
| <img src="https://skillicons.dev/icons?i=nodejs" width="45" alt="Node.js"> | **Node.js** → Criação de servidores rápidos e escaláveis |

</div>

### 🗄️ Banco de Dados  
<div align="center">

| Logo | Descrição |
|------|-----------|
| <img src="https://skillicons.dev/icons?i=mysql" width="45" alt="MySQL"> | **MySQL** → Banco de dados relacional para armazenar informações |

</div>

---

## 🌐 Onde me encontrar
<p align="left">
  <a href="https://www.linkedin.com/in/gustavo-de-lima-máximo-19635 2317" target="_blank">
    <img src="https://skillicons.dev/icons?i=linkedin" width="50" alt="LinkedIn">
  </a>
  <a href="mailto:maximogustavo47@gmail.com">
    <img src="https://skillicons.dev/icons?i=gmail" width="50" alt="E-mail">
  </a>
</p