<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gustavo | Portfólio Front-End</title>

  <link rel="stylesheet" href="style.css">
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>

  <header>
    <h1>Gustavo de Lima Maximo</h1>
    <p>Desenvolvedor Front-End</p>
  </header>

  <main>
    <!-- SOBRE MIM -->
    <section class="card">
      <h2>Sobre mim</h2>
      <p>
        Desenvolvedor front-end focado na criação de interfaces modernas,
        organizadas e responsivas. Possuo experiência com React, HTML, CSS
        e JavaScript, aplicando boas práticas de desenvolvimento e usabilidade.
        Conhecimentos em MySQL e Git para versionamento e organização de projetos.
      </p>
    </section>

    <!-- TECNOLOGIAS -->
    <section class="card">
      <h2>Tecnologias</h2>
      <div class="techs">
        <span>React</span>
        <span>HTML</span>
        <span>CSS</span>
        <span>JavaScript</span>
        <span>MySQL</span>
        <span>Git</span>
      </div>
    </section>

    <!-- GRÁFICO -->
    <section class="card">
      <h2>Linguagens mais usadas nos projetos</h2>
      <canvas id="languagesChart"></canvas>
    </section>
  </main>

  <footer>
    <p>© 2026 • Portfólio GitHub</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", sans-serif;
}

body {
  background: #0f172a;
  color: #e5e7eb;
}

header {
  text-align: center;
  padding: 3rem 1rem;
  background: linear-gradient(135deg, #1e3a8a, #020617);
}

header h1 {
  font-size: 2.6rem;
}

header p {
  margin-top: 0.5rem;
  color: #93c5fd;
}

main {
  max-width: 900px;
  margin: 2rem auto;
  padding: 1rem;
  display: grid;
  gap: 2rem;
}

.card {
  background: #020617;
  padding: 2rem;
  border-radius: 14px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.4);
}

.card h2 {
  margin-bottom: 1rem;
  color: #60a5fa;
}

.techs {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.techs span {
  background: #1e293b;
  padding: 0.7rem 1.2rem;
  border-radius: 10px;
  font-weight: bold;
  transition: 0.3s;
}

.techs span:hover {
  background: #2563eb;
  transform: scale(1.1);
}

footer {
  text-align: center;
  padding: 1.5rem;
  color: #94a3b8;
}

const username = "gustavolmx";
const chartCanvas = document.getElementById("languagesChart");

async function getLanguages() {
  const reposResponse = await fetch(`https://api.github.com/users/${username}/repos`);
  const repos = await reposResponse.json();

  const languageTotals = {};

  for (const repo of repos) {
    if (repo.fork) continue;

    const langResponse = await fetch(repo.languages_url);
    const languages = await langResponse.json();

    for (const lang in languages) {
      languageTotals[lang] = (languageTotals[lang] || 0) + languages[lang];
    }
  }

  return languageTotals;
}

function createChart(languages) {
  const labels = Object.keys(languages);
  const data = Object.values(languages);

  new Chart(chartCanvas, {
    type: "doughnut",
    data: {
      labels,
      datasets: [{
        data,
        borderWidth: 1
      }]
    },
    options: {
      responsive: true,
      animation: {
        duration: 1500
      },
      plugins: {
        legend: {
          position: "bottom"
        }
      }
    }
  });
}

getLanguages().then(createChart);

