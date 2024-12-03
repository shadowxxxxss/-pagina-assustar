# -pagina-assustar
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surpresa!</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            padding-top: 20%;
        }

        .hidden {
            display: none;
        }

        .message {
            font-size: 2em;
        }

        #scare {
            font-size: 4em;
            color: red;
            display: none;
        }
    </style>
</head>
<body>
    <div class="message">Prepare-se para o susto em 3 segundos...</div>
    <div id="scare">VOCÊ VAI PAGAR!!!!!</div>

    <audio id="scream" class="hidden" src="scream.mp3"></audio>

    <script>
        function scare() {
            document.querySelector('.message').style.display = 'none';
            document.getElementById('scare').style.display = 'block';
            document.getElementById('scream').play();
        }

        setTimeout(scare, 3000);
    </script>
</body>
</html>
