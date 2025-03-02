<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>everton</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Arial", sans-serif;
        }

        body {
            text-align: center;
            background-color: #ffebf0;
            color: #333;
            overflow: hidden;
        }

        .container, .game, .declaracao {
            display: none;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            width: 80%;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            animation: fadeIn 1s;
        }

        .active {
            display: block;
        }

        button {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 8px;
            margin: 10px;
        }

        .btn-sim { background-color: #ff4081; color: white; }
        .btn-nao { background-color: #ff1744; color: white; position: absolute; }

        .coracao {
            font-size: 40px;
            cursor: pointer;
            animation: pulse 0.5s infinite alternate;
        }

        .barra {
            width: 50%;
            height: 20px;
            background: #ddd;
            border-radius: 10px;
            overflow: hidden;
            margin: 20px auto;
        }

        .progresso {
            height: 100%;
            width: 0%;
            background: #ff4081;
            transition: width 0.2s;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, -55%); }
            to { opacity: 1; transform: translate(-50%, -50%); }
        }

        @keyframes floatHearts {
            from { transform: translateY(0); opacity: 1; }
            to { transform: translateY(-200px); opacity: 0; }
        }

        .heart {
            position: absolute;
            color: red;
            font-size: 20px;
            animation: floatHearts 3s linear infinite;
        }
    </style>
</head>
<body>
    <div class="container active" id="intro">
       <p>Oii querido! Queria te dar um presente diferente e, depois de pensar muito, resolvi fazer isso.<br>
        Eu poderia ter feito de uma forma melhor, mas, você sabe, sou ansiosa e queria te entregar hoje.<br>
        Então, aqui está! Você aceita continuar?</p>
        <button class="btn-sim" onclick="mostrar('pergunta')">Sim</button>
        <button class="btn-nao" onmouseover="fugir()">Não</button>
    </div>

    <div class="container" id="pergunta">
        <p>Qual a data de nascimento do amor da tua vida? 💖</p>
        <button onclick="responder(false)">27/12/2006</button>
        <button onclick="responder(false)">21/12/2006</button>
        <button onclick="responder(true)">23/12/2006</button>
    </div>

    <div class="game" id="jogo">
        <p>Clique no coração para encher a barra de amor! 💖</p>
        <div class="barra">
            <div class="progresso" id="barra"></div>
        </div>
        <span class="coracao" onclick="aumentarAmor()">❤️</span>
        <br>
        <button onclick="finalizar()">Enviar porcentagem</button>
    </div>

    <div class="declaracao" id="final">
        <h2>💖 Minha Declaração 💖</h2>
        <p>Quero te dizer algo que está no meu coração, algo simples, mas que carrega um significado imenso: eu te amo. Amo a forma como você me faz sentir única, como tudo ao meu redor parece mais bonito quando você está por perto. Amo o jeito que você me olha, o jeito que cuida de mim, mesmo nas pequenas coisas do dia a dia.É impressionante como, com você, os momentos se tornam especiais. Sua presença me traz uma paz que eu não sabia que existia, e cada risada compartilhada, cada conversa, se tornam memórias que guardo com muito carinho.Eu te amo por quem você é, pela pessoa incrível que você se mostrou ser, pelo respeito, pelo carinho e pela paciência. Eu te amo porque ao seu lado, eu posso ser completamente eu, e isso é algo raro e precioso.Eu não preciso de mais nada, porque com você, tudo faz sentido. Te amo de uma forma tão verdadeira que as palavras ficam pequenas para expressar o que sinto. Só sei que ao te amar, encontro a felicidade que eu sempre procurei</p>
        <button class="btn-sim"><a href="https://freeimage.host/i/32tKtNR" download="Certificado do Amor" style="color: white; text-decoration: none;">Gerar Certificado</a></button>
    </div>

    <script>
        function mostrar(id) {
            document.querySelector('.active').classList.remove('active');
            document.getElementById(id).classList.add('active');
        }

        function responder(correto) {
            if (correto) {
                mostrar('jogo');
            } else {
                alert("Errado! Tente de novo. 🤨");
            }
        }

        function fugir() {
            let btn = document.querySelector(".btn-nao");
            let x = Math.random() * window.innerWidth - 100;
            let y = Math.random() * window.innerHeight - 50;
            btn.style.left = `${x}px`;
            btn.style.top = `${y}px`;
        }

        let amor = 0;
        function aumentarAmor() {
            if (amor < 100) {
                amor += 10;
                document.getElementById("barra").style.width = amor + "%";
                criarCoracao();
            }
        }

        function finalizar() {
            if (amor >= 100) {
                mostrar('final');
            } else {
                alert("Nossa, achei que você me amava mais... 😢");
            }
        }

        function criarCoracao() {
            let coracao = document.createElement("div");
            coracao.classList.add("heart");
            coracao.innerHTML = "❤️";
            coracao.style.left = Math.random() * window.innerWidth + "px";
            coracao.style.top = "100vh";
            document.body.appendChild(coracao);
            setTimeout(() => coracao.remove(), 3000);
        }
    </script>
</body>
</html>
