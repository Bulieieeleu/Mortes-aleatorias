<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>O Fim Aleatório</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #111;
      color: #fff;
      text-align: center;
      padding-top: 50px;
    }
    button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #ff4444;
      border: none;
      border-radius: 8px;
      color: white;
      cursor: pointer;
      margin-bottom: 30px;
    }
    .resultado {
      font-size: 24px;
      margin-top: 20px;
    }
    .aviso {
      margin-top: 40px;
      font-size: 14px;
      color: #aaa;
    }
  </style>
</head>
<body>

  <h1>Descubra como "alguém" morreu</h1>
  <button onclick="gerarMorte()">Mostrar Morte Aleatória</button>

  <div class="resultado" id="resultado"></div>
  <div class="aviso">Nada nesse site é real. É tudo fictício, idiota e feito para rir. Ninguém mencionado aqui morreu de verdade.</div>

  <script>
    const nomes = [
      "João Vitor", "Gabriela Souza", "Lucas Lima", "Ana Beatriz", "Carlos Henrique",
      "Pedro Paulo", "Jéssica Silva", "Tiago Oliveira", "Juliana Alves", "Felipe Santos"
    ];

    const mortesEngracadas = [
      "foi esmagado por uma geladeira que caiu do céu",
      "tentou dançar funk no topo de um caminhão em movimento",
      "confundiu supercola com enxaguante bucal",
      "entrou em briga com um pato e perdeu",
      "comeu 50 pães em 2 minutos e explodiu",
      "morreu tentando lamber o próprio cotovelo",
      "gritou 'EU VOO!' e pulou do sofá",
      "tentou domar um javali com voz suave",
      "achou que era uma boa ideia brincar com uma colmeia",
      "se escondeu na máquina de lavar durante esconde-esconde"
    ];

    const sons = [
      "https://www.myinstants.com/media/sounds/windows-xp-error.mp3",
      "https://www.myinstants.com/media/sounds/vine-boom.mp3",
      "https://www.myinstants.com/media/sounds/mario.mp3",
      "https://www.myinstants.com/media/sounds/metal-pipe-clang.mp3"
    ];

    function gerarMorte() {
      const nome = nomes[Math.floor(Math.random() * nomes.length)];
      const idade = Math.floor(Math.random() * 90) + 10;
      const morte = mortesEngracadas[Math.floor(Math.random() * mortesEngracadas.length)];
      const som = new Audio(sons[Math.floor(Math.random() * sons.length)]);
      som.play();

      document.getElementById("resultado").innerHTML = `${nome}, com ${idade} anos, ${morte}.`;
    }
  </script>

</body>
</html>
