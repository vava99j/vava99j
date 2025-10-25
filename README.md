<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8"/>
  <meta http-equiv="X-UA-Compatible" content="IE=edge"/>
  <meta name="viewport" content="width=device-width, initial-scale=1"/>
  <title>Home | Tec-Hor</title>
  <link rel="shortcut icon" href="assets/images/47b3204c-f074-4262-87dc-d95bf20c03d6-removebg-preview-1.png" type="image/x-icon"/>

  <!-- CSS embutido -->
  <style>
    :root {
      --verde: #28a745;
      --fundo-claro: #f8f9fa;
      --fundo-escuro: #1c1c1c;
      --texto-claro: #f1f1f1;
      --texto-escuro: #333;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: "Poppins", sans-serif;
    }

    body.light-mode {
      background-color: var(--fundo-claro);
      color: var(--texto-escuro);
      transition: 0.4s;
    }

    body.dark-mode {
      background-color: var(--fundo-escuro);
      color: var(--texto-claro);
      transition: 0.4s;
    }

    /* NAVBAR */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background-color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 10px 50px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      z-index: 10;
    }

    .navbar img {
      height: 60px;
    }

    .navbar ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    .navbar ul li a {
      text-decoration: none;
      color: var(--verde);
      font-weight: 600;
      transition: 0.3s;
    }

    .navbar ul li a:hover {
      color: #1e7e34;
    }

    .navbar .buttons {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .navbar button, .navbar a.btn {
      padding: 8px 15px;
      border: 2px solid var(--verde);
      border-radius: 6px;
      background: none;
      cursor: pointer;
      transition: 0.3s;
      font-weight: 600;
    }

    .navbar button:hover, .navbar a.btn:hover {
      background-color: var(--verde);
      color: white;
    }

    .navbar a.btn {
      background-color: var(--verde);
      color: white;
      text-decoration: none;
    }

    /* CABEÇALHO */
    header {
      text-align: center;
      padding-top: 130px;
    }

    header h1 {
      color: var(--verde);
      font-size: 4rem;
      font-weight: 700;
    }

    header p {
      color: #666;
      font-size: 1.5rem;
      margin-bottom: 20px;
    }

    header img {
      max-width: 80%;
      border-radius: 20px;
      border: 4px solid var(--verde);
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    }

    /* SEÇÃO DE VANTAGENS */
    section {
      text-align: center;
      padding: 60px 20px;
    }

    section h2 {
      color: var(--verde);
      margin-bottom: 40px;
      font-size: 2rem;
    }

    .cards {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 30px;
    }

    .card {
      background-color: white;
      width: 300px;
      padding: 20px;
      border-radius: 20px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .card img {
      width: 100%;
      border-radius: 15px;
      margin-bottom: 15px;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }

    .card h5 {
      color: var(--verde);
      margin-bottom: 10px;
    }

    .card p {
      color: #666;
    }

    /* SOBRE O PROJETO */
    .sobre {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-wrap: wrap;
      gap: 40px;
      padding: 60px 20px;
    }

    .sobre img {
      width: 400px;
      border-radius: 20px;
      box-shadow: 0 5px 20px rgba(0,0,0,0.1);
    }

    .sobre-texto {
      max-width: 500px;
      text-align: left;
    }

    .sobre-texto h2 {
      color: var(--verde);
      margin-bottom: 20px;
    }

    .sobre-texto p {
      color: #666;
      line-height: 1.6;
    }

    .sobre-texto a {
      display: inline-block;
      margin-top: 15px;
      background-color: var(--verde);
      color: white;
      padding: 10px 20px;
      border-radius: 8px;
      text-decoration: none;
      transition: 0.3s;
    }

    .sobre-texto a:hover {
      background-color: #1e7e34;
    }

    /* RODAPÉ */
    footer {
      text-align: center;
      padding: 20px;
      border-top: 1px solid #ccc;
      color: #777;
    }

    /* DARK MODE */
    body.dark-mode .navbar {
      background-color: #2b2b2b;
    }

    body.dark-mode .card {
      background-color: #2f2f2f;
      color: var(--texto-claro);
    }

    body.dark-mode .navbar ul li a {
      color: #9ae6b4;
    }

    body.dark-mode .sobre-texto p {
      color: #ddd;
    }

    /* RESPONSIVO */
    @media (max-width: 768px) {
      .navbar {
        flex-direction: column;
        padding: 15px;
      }

      .navbar ul {
        flex-direction: column;
        gap: 10px;
      }

      header h1 {
        font-size: 2.5rem;
      }

      .sobre {
        flex-direction: column;
      }

      .card {
        width: 90%;
      }

      .Estufa{
        width: 50%;
      }
    }
  </style>
</head>

<body class="light-mode">
  <!-- NAVBAR -->
  <nav class="navbar">
    <a href="index.html">
      <img src="img/icon.png" alt="Logo">
    </a>
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="sobre.html">Sobre Nós</a></li>
      <li><a href="infos.html">Infos Técnicas</a></li>
    </ul>
    <div class="buttons">
      <button id="modeToggle">🌙</button>
      <a href="contato.html" class="btn">Contacte-nos</a>
    </div>
  </nav>

  <!-- CABEÇALHO -->
  <header>
    <h1>Tec-Hor</h1>
    <p>Estufa Inteligente 🌱</p>
    <img src="img/ftestufa.png" alt="Estufa" class="Estufa">
  </header>

  <!-- SEÇÃO DE VANTAGENS -->
  <section>
    <h2>Por que escolher a Tec-Hor?</h2>
    <div class="cards">
      <div class="card">
        <img src="img/regação.jpg" alt="Rega automática">
        <h5>Rega Automática</h5>
        <p>Fique fora de casa sem se preocupar com a água da sua plantação.</p>
      </div>

      <div class="card">
        <img src="img/sol.jpg" alt="Crescimento acelerado">
        <h5>Crescimento Acelerado</h5>
        <p>A estufa cria o ambiente perfeito, aumentando a velocidade de crescimento das plantas.</p>
      </div>

      <div class="card">
        <img src="img/gallery6.jpg" alt="Informações sobre a planta">
        <h5>Informações da Planta</h5>
        <p>Acompanhe tudo pelo aplicativo, com dicas e dados sobre cada espécie cultivada.</p>
      </div>
    </div>
  </section>

  <!-- SOBRE O PROJETO -->
  <section class="sobre">
    <img src="img/icon.png" alt="Projeto">
    <div class="sobre-texto">
      <h2>Sobre o Projeto</h2>
      <p>
        A estufa automática oferece autonomia total, cuidando das plantas sem necessidade de rega manual.
        Ela ajusta luz, temperatura, irrigação e outros fatores com base no histórico de crescimento.
        Também permite personalizar o ambiente para cada planta e se integrar com assistentes virtuais
        como Alexa ou Google Assistant — facilitando o controle por voz ou celular.
      </p>
      <a href="contato.html">Contacte-nos</a>
    </div>
  </section>

  <!-- RODAPÉ -->
  <footer>
    <p>© 2025 Tec-Hor | Todos os direitos reservados 💚</p>
  </footer>

  <!-- Script modo escuro -->
  <script>
    const toggleBtn = document.getElementById("modeToggle");
    const body = document.body;

    toggleBtn.addEventListener("click", () => {
      body.classList.toggle("dark-mode");
      body.classList.toggle("light-mode");
      toggleBtn.textContent = body.classList.contains("dark-mode") ? "🌞" : "🌙";
    });
  </script>
</body>
</html>
