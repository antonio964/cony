<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reproducir Video</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: Arial, sans-serif;
            flex-direction: column;
            color: white;
            overflow: hidden; /* Evita el scroll */
        }

        video#backgroundVideo {
            position: fixed;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: -1;
            transform: translate(-50%, -50%);
        }

        .button-container {
            text-align: center;
            margin-bottom: 20px;
            z-index: 1; /* Asegura que el botón esté encima del fondo */
        }

        button {
            padding: 15px 30px;
            font-size: 18px;
            color: white;
            background-color: #007BFF;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            z-index: 1;
        }

        button:hover {
            background-color: #0056b3;
        }

        video#miVideo {
            display: none;
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            z-index: 9999;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5); /* Oscurece un poco el fondo */
            z-index: 0;
        }
    </style>
</head>
<body>
    <video id="backgroundVideo" autoplay muted loop>
        <source src="fondo.mp4" type="video/mp4">
        Tu navegador no soporta la reproducción de videos.
    </video>

    <div class="overlay"></div>

    <div class="button-container">
        <h1>ᴄᴏɴʏ ᴄʜᴜᴘᴀᴘɪɴɢᴀ ᴄʜᴇᴄᴀ ᴇꜱᴛᴏ ᴏ ᴇʀᴇɪ ɢᴀɪ?</h1>
        <button onclick="mostrarVideo()">Ver Video</button>
    </div>
    
    <video id="miVideo" controls>
        <source src="video.mp4" type="video/mp4">
        Tu navegador no soporta la reproducción de videos.
    </video>

    <script>
        function mostrarVideo() {
            var video = document.getElementById('miVideo');
            video.style.display = 'block';
            video.play();
            video.requestFullscreen();
        }
    </script>
</body>
</html>

