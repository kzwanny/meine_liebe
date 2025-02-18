<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meine_Lieb</title>
    <style>
        body {
            background-color: #f7c6d1;
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        h1 {
            font-size: 3rem;
            color: #ffffff;
            text-align: center;
            animation: fadeIn 3s ease-in-out;
        }

        /* Animação para o fade in do texto */
        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }

        /* Adicionando fontes bonitas */
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');
    </style>
</head>
<body>
    <h1 id="message">Amo você, princesinha Ivy Belle</h1>

    <!-- Script para os fogos de artifício -->
    <script>
        // Função para criar fogos de artifício
        function createFireworks() {
            const numFireworks = 10; // Número de fogos de artifício
            const colors = ['#ff69b4', '#ff1493', '#ff00ff', '#ff6347', '#ff4500']; // Cores dos fogos de artifício

            for (let i = 0; i < numFireworks; i++) {
                let firework = document.createElement('div');
                firework.style.position = 'absolute';
                firework.style.borderRadius = '50%';
                firework.style.width = '10px';
                firework.style.height = '10px';
                firework.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                firework.style.animation = `firework-animation ${Math.random() * 2 + 2}s ease-out`;

                firework.style.left = `${Math.random() * 100}%`;
                firework.style.top = `${Math.random() * 100}%`;
                document.body.appendChild(firework);

                setTimeout(() => {
                    firework.remove();
                }, 2000); // Remove os fogos de artifício após 2 segundos
            }
        }

        // Função para animação dos fogos de artifício
        setInterval(createFireworks, 1500);
    </script>

    <!-- Adicionando animação CSS para o efeito de explosão dos fogos -->
    <style>
        @keyframes firework-animation {
            0% {
                transform: scale(0);
                opacity: 1;
            }
            50% {
                transform: scale(1.5);
                opacity: 0.7;
            }
            100% {
                transform: scale(0);
                opacity: 0;
            }
        }
    </style>
</body>
</html>
