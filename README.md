<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz 2 Meses de Namoro</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden; /* Para esconder elementos que saem da tela */
        }
        h2 {
            color: #e63946;
            margin-top: 20px;
            font-size: 18px;
            padding: 0 10px; /* Adiciona espaçamento nas laterais */
            z-index: 5; /* Para garantir que o texto fique acima */
        }
        h1 {
            color: #e63946;
            margin-top: 20px;
            font-size: 28px; /* Aumenta o tamanho da fonte */
            z-index: 5; /* Para garantir que o texto fique acima */
        }
        img {
            width: 90%; /* Ajusta a imagem para caber na tela do celular */
            max-width: 400px; /* Limita a largura máxima */
            height: auto;
            margin-top: 10px; /* Espaço entre a imagem e o texto */
        }
        .floating-image {
            position: absolute;
            width: 100px; /* Tamanho da imagem flutuante */
            animation: float 5s infinite;
            z-index: 10; /* Para garantir que fique acima de outros elementos */
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-50px); }
            100% { transform: translateY(0); }
        }
    </style>
</head>
<body>
    <img src="https://uploads.spiritfanfiction.com/historias/capitulos/201703/dragoes-aventuras-alem-do-arquipelago-8443490-220320171516.png" alt="Imagem do Filme">
    <h2>Astrid, a gente já passou por... muita coisa junto, você acha que a gente não vai lidar com isso? - lembrei que você gosta muito desse filme.</h2>
    <h1>Feliz 2 meses de namoro, meu docinho! Eu amo você!</h1>

    <script>
        function createFloatingHeart() {
            const heart = document.createElement('img');
            heart.className = 'floating-image';
            heart.src = 'https://static.vecteezy.com/ti/vetor-gratis/p1/2513330-red-heart-pixel-art-vetor.jpg';
            heart.alt = 'Coração Flutuante';
            
            // Definindo limites para a posição do coração
            const maxX = window.innerWidth - 100; // Largura da tela menos a largura do coração
            const maxY = window.innerHeight - 300; // Altura da tela menos a altura do texto

            heart.style.left = Math.random() * maxX + 'px'; // Posição horizontal aleatória
            heart.style.top = Math.random() * maxY + 'px'; // Posição vertical aleatória
            heart.style.animationDuration = (Math.random() * 3 + 2) + 's'; // Duração da animação aleatória

            document.body.appendChild(heart);

            // Remove o coração após a animação
            setTimeout(() => {
                heart.remove();
            }, 5000); // Tempo que o coração leva para sair da tela
        }

        // Cria um novo coração a cada 500ms
        setInterval(createFloatingHeart, 500);
    </script>
</body>
</html>
