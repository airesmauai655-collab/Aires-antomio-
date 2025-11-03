<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JNJH Shop</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #f7f7f7, #e0f2f1);
      margin: 0;
      padding: 0;
      color: #333;
    }

    header {
      background-color: #00796b;
      color: white;
      text-align: center;
      padding: 30px 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }

    main {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px 10px;
    }

    .produto {
      background-color: white;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      max-width: 400px;
      padding: 25px;
      text-align: center;
      margin-bottom: 30px;
    }

    img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 20px;
    }

    h2 {
      color: #00796b;
    }

    .preco {
      font-size: 1.5em;
      font-weight: bold;
      color: #004d40;
    }

    button {
      background-color: #00796b;
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #004d40;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #004d40;
      color: white;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <header>
    <h1>JNJH Shop</h1>
    <p>Conhecimento que transforma!</p>
  </header>

  <main>
    <div class="produto">
      <img src="https://picsum.photos/400/250" alt="Imagem do produto">
      <h2>JMJH Curso Online</h2>
      <p>Conhecimento que transforma! Acesse conteúdo exclusivo com <strong>direito PLR</strong>: aprenda, use e revenda. Invista em você e crie sua própria renda. <em>Comece agora!</em></p>
      <p class="preco">💰 1.580 MT</p>
      <a href="https://wa.me/258869644130?text=Olá! Quero comprar o JMJH Curso Online por 1580MT.">
        <button>Comprar no WhatsApp</button>
      </a>
    </div>
  </main>

  <footer>
    &copy; 2025 JNJH Shop — Todos os direitos reservados
  </footer>

</body>
</html>
