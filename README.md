<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Santos Acessível e Inteligente</title>
  <style>
    :root {
      --primary-color: #0056b3;
      --secondary-color: #0088cc;
      --bg-color: #f4f7f6;
      --text-color: #333333;
      --card-bg: #ffffff;
    }

    /* Estilos de Alto Contraste */
    body.high-contrast {
      --primary-color: #ffff00;
      --secondary-color: #ffff00;
      --bg-color: #000000;
      --text-color: #ffffff;
      --card-bg: #1a1a1a;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      line-height: 1.6;
      transition: background-color 0.3s, color 0.3s;
    }

    /* Barra de Acessibilidade */
    .accessibility-bar {
      background-color: #222;
      color: #fff;
      padding: 10px 20px;
      display: flex;
      justify-content: flex-end;
      gap: 15px;
    }

    .accessibility-bar button {
      background: none;
      border: 1px solid #fff;
      color: #fff;
      padding: 5px 10px;
      cursor: pointer;
      border-radius: 4px;
      font-weight: bold;
    }

    .accessibility-bar button:hover {
      background: #fff;
      color: #222;
    }

    /* Cabeçalho */
    header {
      background-color: var(--primary-color);
      color: white;
      padding: 40px 20px;
      text-align: center;
    }

    header h1 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    /* Conteúdo Principal */
    container {
      display: block;
      max-width: 1100px;
      margin: 30px auto;
      padding: 0 20px;
    }

    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .card {
      background-color: var(--card-bg);
      border-radius: 8px;
      padding: 25px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      border-top: 5px solid var(--primary-color);
    }

    .card h3 {
      margin-bottom: 15px;
      font-size: 1.4rem;
    }

    /* Rodapé */
    footer {
      text-align: center;
      padding: 20px;
      background-color: #222;
      color: white;
      margin-top: 50px;
    }
  </style>
</head>
<body>

  <!-- Barra de Acessibilidade -->
  <div class="accessibility-bar" aria-label="Ferramentas de acessibilidade">
    <button onclick="toggleContrast()">Alto Contraste</button>
    <button onclick="changeFontSize(1)">A+</button>
    <button onclick="changeFontSize(-1)">A-</button>
  </div>

  <!-- Cabeçalho Principal -->
  <header>
    <h1>Santos Acessível e Inteligente</h1>
    <p>Tecnologia, Inclusão e Mobilidade para Toda a Cidade</p>
  </header>

  <!-- Conteúdo -->
  <container>
    <section>
      <h2>Sobre o Projeto</h2>
      <p>Iniciativa voltada para promover a acessibilidade urbanística, transporte adaptado e integração de tecnologias inteligentes na cidade de Santos.</p>
    </section>

    <div class="features-grid">
      <div class="card">
        <h3>♿ Mobilidade Inclusiva</h3>
        <p>Rotas acessíveis, calçadas niveladas e transporte público adaptado com suporte em tempo real.</p>
      </div>

      <div class="card">
        <h3>💡 Cidade Inteligente</h3>
        <p>Semáforos sonoros interativos, sensores de tráfego e sinalização digital acessível.</p>
      </div>

      <div class="card">
        <h3>📱 Tecnologia Assistiva</h3>
        <p>Aplicativos e plataformas para orientação em espaços públicos e turísticos da cidade.</p>
      </div>
    </div>
  </container>

  <footer>
    <p>&copy; Santos Acessível e Inteligente - Projeto Urbano</p>
  </footer>

  <!-- Script de Interatividade -->
  <script>
    function toggleContrast() {
      document.body.classList.toggle('high-contrast');
    }

    let currentFontSize = 100;
    function changeFontSize(delta) {
      currentFontSize += delta * 10;
      if (currentFontSize >= 70 && currentFontSize <= 150) {
        document.body.style.fontSize = currentFontSize + '%';
      }
    }
  </script>
</body>
</html>
