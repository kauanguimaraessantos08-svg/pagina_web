<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Era de Ouro - Vôlei Masculino Brasileiro</title>
  <style>
    :root {
      --primary: #183C63;
      --accent: #FFD700;
      --secondary: #009c3b;
      --bg-light: #F4F7FA;
      --card-bg: #FFFFFF;
      --text-dark: #2C3E50;
      --text-muted: #6C757D;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--bg-light);
      color: var(--text-dark);
      line-height: 1.6;
    }

    /* HEADER */
    header {
      background: linear-gradient(135deg, #183C63 0%, #0D233A 100%);
      color: #FFFFFF;
      text-align: center;
      padding: 40px 20px;
      border-bottom: 5px solid var(--accent);
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }

    .header-content {
      max-width: 900px;
      margin: 0 auto;
    }

    header h1 {
      font-size: 2.5rem;
      margin-bottom: 15px;
      color: #FFFFFF;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    header p {
      font-size: 1.1rem;
      color: #E2E8F0;
      max-width: 750px;
      margin: 0 auto;
    }

    /* BARRA DE PESQUISA E FILTROS */
    .controls {
      max-width: 900px;
      margin: 25px auto -20px auto;
      padding: 0 20px;
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
    }

    .search-box {
      flex: 1;
      min-width: 250px;
    }

    .search-box input {
      width: 100%;
      padding: 12px 18px;
      border: 2px solid #CBD5E1;
      border-radius: 30px;
      font-size: 1rem;
      outline: none;
      transition: border-color 0.3s;
    }

    .search-box input:focus {
      border-color: var(--primary);
    }

    .filter-buttons {
      display: flex;
      gap: 8px;
    }

    .filter-btn {
      background-color: #E2E8F0;
      border: none;
      padding: 8px 16px;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
      color: var(--primary);
      transition: all 0.3s;
    }

    .filter-btn.active, .filter-btn:hover {
      background-color: var(--primary);
      color: #FFFFFF;
    }

    /* CONTEÚDO PRINCIPAL */
    main {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 20px;
      display: flex;
      flex-direction: column;
      gap: 25px;
    }

    /* CARD DE ARTIGO */
    article {
      background-color: var(--card-bg);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 15px rgba(0,0,0,0.06);
      display: flex;
      flex-direction: column;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    @media (min-width: 650px) {
      article {
        flex-direction: row;
      }
    }

    article:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 25px rgba(0,0,0,0.1);
    }

    .article-img-container {
      width: 100%;
      height: 200px;
      background-color: #E2E8F0;
      flex-shrink: 0;
    }

    @media (min-width: 650px) {
      .article-img-container {
        width: 220px;
        height: auto;
      }
    }

    .article-img-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .article-content {
      padding: 20px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      flex-grow: 1;
    }

    .tag {
      align-self: flex-start;
      background-color: #E0F2FE;
      color: #0369A1;
      font-size: 0.75rem;
      font-weight: bold;
      padding: 4px 10px;
      border-radius: 12px;
      margin-bottom: 8px;
      text-transform: uppercase;
    }

    article h2 {
      font-size: 1.35rem;
      color: var(--primary);
      margin-bottom: 6px;
    }

    .artigo-autor {
      font-size: 0.85rem;
      color: var(--text-muted);
      font-weight: 600;
      margin-bottom: 12px;
    }

    .article-text {
      font-size: 0.95rem;
      color: #475569;
      margin-bottom: 16px;
      flex-grow: 1;
    }

    /* BOTÕES DE REAÇÃO */
    .article-actions {
      display: flex;
      gap: 12px;
      border-top: 1px solid #F1F5F9;
      padding-top: 12px;
    }

    .reaction-btn {
      background-color: #F8FAFC;
      border: 1px solid #E2E8F0;
      padding: 6px 14px;
      border-radius: 20px;
      cursor: pointer;
      font-size: 0.9rem;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.2s ease;
      color: var(--text-dark);
    }

    .reaction-btn:hover {
      background-color: #EDF2F7;
    }

    .reaction-btn.active-heart {
      background-color: #FFE4E6;
      border-color: #FDA4AF;
      color: #E11D48;
    }

    .reaction-btn.active-like {
      background-color: #E0F2FE;
      border-color: #7DD3FC;
      color: #0284C7;
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 25px;
      background-color: var(--primary);
      color: #FFFFFF;
      font-size: 0.9rem;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header>
    <div class="header-content">
      <h1>Era de Ouro do Vôlei Masculino</h1>
      <p>A trajetória inesquecível da Seleção Brasileira nos anos 2000: o time sob o comando de Bernardinho que dominou o planeta e reescreveu a história do esporte mundial.</p>
    </div>
  </header>

  <!-- Filtros e Busca -->
  <div class="controls">
    <div class="search-box">
      <input type="text" id="searchInput" placeholder="Pesquisar atleta, conquista ou assunto...">
    </div>
    <div class="filter-buttons">
      <button class="filter-btn active" onclick="filterArticles('all')">Todos</button>
      <button class="filter-btn" onclick="filterArticles('historia')">História</button>
      <button class="filter-btn" onclick="filterArticles('jogadores')">Jogadores</button>
      <button class="filter-btn" onclick="filterArticles('titulos')">Títulos</button>
    </div>
  </div>

  <main id="newsContainer">

    <!-- Notícia 1: Visão Geral -->
    <article data-category="historia">
      <div class="article-img-container">
        <img src="https://images.unsplash.com/photo-1592656094267-764a45160876?auto=format&fit=crop&w=400&q=80" alt="Quadra de Vôlei">
      </div>
      <div class="article-content">
        <div>
          <span class="tag">História</span>
          <h2>A Hegemonia de uma Geração Inesquecível</h2>
          <p class="artigo-autor">Por: Redação do Vôlei</p>
          <p class="article-text">Sob o comando técnico de Bernardinho, a seleção brasileira masculina de vôlei construiu nos anos 2000 a era mais dominante da história do esporte. Com um padrão tático inovador, velocidade impressionante e disciplina física, o Brasil disputou praticamente todas as finais de grandes torneios entre 2001 e 2010.</p>
        </div>
        <div class="article-actions">
          <button class="reaction-btn heart-btn">❤️ <span>12</span></button>
          <button class="reaction-btn like-btn">👍 <span>34</span></button>
        </div>
      </div>
    </article>

    <!-- Notícia 2: Giba -->
    <article data-category="jogadores">
      <div class="article-img-container">
        <img src="https://images.unsplash.com/photo-1612872087720-bb876e2e67d1?auto=format&fit=crop&w=400&q=80" alt="Jogador de Vôlei na rede">
      </div>
      <div class="article-content">
        <div>
          <span class="tag">Jogadores</span>
          <h2>Giba: O Protagonista e Símbolo de uma Era</h2>
          <p class="artigo-autor">Por: Redação do Vôlei</p>
          <p class="article-text">O camisa 7 foi a grande cara dessa geração. Camisa de força, velocidade incrível no ataque de ponta e capacidade decisiva nos momentos sob pressão. Giba foi eleito MVP (Melhor Jogador) das Olimpíadas de Atenas 2004 e do Mundial de 2006, consolidando-se como lenda internacional.</p>
        </div>
        <div class="article-actions">
          <button class="reaction-btn heart-btn">❤️ <span>25</span></button>
          <button class="reaction-btn like-btn">👍 <span>50</span></button>
        </div>
      </div>
    </article>

    <!-- Notícia 3: Serginho Escadinha -->
    <article data-category="jogadores">
      <div class="article-img-container">
        <img src="https://images.unsplash.com/photo-1579952363873-27f3bade9f55?auto=format&fit=crop&w=400&q=80" alt="Vôlei em ação">
      </div>
      <div class="article-content">
        <div>
          <span class="tag">Jogadores</span>
          <h2>Serginho "Escadinha": A Revolução do Líbero</h2>
          <p class="artigo-autor">Por: Redação do Vôlei</p>
          <p class="article-text">Reconhecido mundialmente como o maior líbero da história do vôlei. Serginho transformou a defesa em arte, garantindo recepções perfeitas e passes precisos que permitiam o jogo rápido do Brasil. Mais tarde, viria a ser eleito o MVP dos Jogos Olímpicos de 2016.</p>
        </div>
        <div class="article-actions">
          <button class="reaction-btn heart-btn">❤️ <span>18</span></button>
          <button class="reaction-btn like-btn">👍 <span>42</span></button>
        </div>
      </div>
    </article>

    <!-- Notícia 4: Ricardinho -->
    <article data-category="jogadores">
      <div class="article-img-container">
        <img src="https://images.unsplash.com/photo-1547347298-1d74850a1ae7?auto=format&fit=crop&w=400&q=80" alt="Bola de Vôlei">
      </div>
      <div class="article-content">
        <div>
          <span class="tag">Jogadores</span>
          <h2>Ricardinho: A Mente Brilhante do Levantamento</h2>
          <p class="artigo-autor">Por: Redação do Vôlei</p>
          <p class="article-text">Famoso por acelerar a distribuição de jogo a níveis nunca antes vistos. Ricardinho enganava o bloqueio adversário com passes rápidos de costas e jogadas pelo meio, sendo peça vital no ouro de Atenas 2004 e no tricampeonato mundial.</p>
        </div>
        <div class="article-actions">
          <button class="reaction-btn heart-btn">❤️ <span>9</span></button>
          <button class="reaction-btn like-btn">👍 <span>21</span></button>
        </div>
      </div>
    </article>

    <!-- Notícia 5: Títulos -->
    <article data-category="titulos">
      <div class="article-img-container">
        <img src="https://images.unsplash.com/photo-1562552052-c72ceddf93dc?auto=format&fit=crop&w=400&q=80" alt="Medalhas e Troféus">
      </div>
      <div class="article-content">
        <div>
          <span class="tag">Títulos</span>
          <h2>A Galeria de Conquistas Impressionante</h2>
          <p class="artigo-autor">Por: Redação do Vôlei</p>
          <p class="article-text">Durante o ciclo de ouro, o Brasil conquistou: Ouro Olímpico (Atenas 2004), Pratas Olímpicas (Pequim 2008 e Londres 2012), Tricampeonato Mundial (2002, 2006, 2010), além de 7 títulos da Liga Mundial e duas Copas do Mundo.</p>
        </div>
        <div class="article-actions">
          <button class="reaction-btn heart-btn">❤️ <span>30</span></button>
          <button class="reaction-btn like-btn">👍 <span>65</span></button>
        </div>
      </div>
    </article>

  </main>

  <footer>
    <p>&copy; Portal da Era de Ouro do Vôlei Brasileiro - Projeto Educativo</p>
  </footer>

  <script>
    // LÓGICA DOS BOTÕES DE REAÇÃO (CURTIDAS)
    const articles = document.querySelectorAll("article");

    articles.forEach(article => {
      const heartBtn = article.querySelector(".heart-btn");
      const likeBtn = article.querySelector(".like-btn");

      if (heartBtn) {
        let heartActive = false;
        heartBtn.addEventListener("click", () => {
          const span = heartBtn.querySelector("span");
          let count = parseInt(span.textContent);
          if (!heartActive) {
            span.textContent = count + 1;
            heartBtn.classList.add("active-heart");
            heartActive = true;
          } else {
            span.textContent = count - 1;
            heartBtn.classList.remove("active-heart");
            heartActive = false;
          }
        });
      }

      if (likeBtn) {
        let likeActive = false;
        likeBtn.addEventListener("click", () => {
          const span = likeBtn.querySelector("span");
          let count = parseInt(span.textContent);
          if (!likeActive) {
            span.textContent = count + 1;
            likeBtn.classList.add("active-like");
            likeActive = true;
          } else {
            span.textContent = count - 1;
            likeBtn.classList.remove("active-like");
            likeActive = false;
          }
        });
      }
    });

    // LÓGICA DE FILTRAGEM POR CATEGORIA
    function filterArticles(category) {
      const filterBtns = document.querySelectorAll(".filter-btn");
      filterBtns.forEach(btn => btn.classList.remove("active"));
      event.target.classList.add("active");

      articles.forEach(article => {
        const articleCategory = article.getAttribute("data-category");
        if (category === "all" || articleCategory === category) {
          article.style.display = "flex";
        } else {
          article.style.display = "none";
        }
      });
    }

    // LÓGICA DA BARRA DE PESQUISA EM TEMPO REAL
    const searchInput = document.getElementById("searchInput");
    searchInput.addEventListener("input", function() {
      const query = this.value.toLowerCase();

      articles.forEach(article => {
        const title = article.querySelector("h2").textContent.toLowerCase();
        const text = article.querySelector(".article-text").textContent.toLowerCase();

        if (title.includes(query) || text.includes(query)) {
          article.style.display = "flex";
        } else {
          article.style.display = "none";
        }
      });
    });
  </script>
</body>
</html>