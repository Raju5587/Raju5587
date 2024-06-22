<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>YouTube Clone</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        header {
            width: 100%;
            background-color: #FF0000;
            color: white;
            display: flex;
            justify-content: space-between;
            padding: 10px 20px;
            align-items: center;
        }
        header img {
            cursor: pointer;
        }
        #main-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-top: 20px;
        }
        #video-container {
            width: 560px;
            height: 315px;
            margin-bottom: 20px;
        }
        #form-container {
            display: none;
            flex-direction: column;
            align-items: center;
            margin-top: 20px;
        }
        .button {
            background-color: #FF0000;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            margin: 5px;
        }
    </style>
</head>
<body>

    <header>
        <img src="https://www.youtube.com/img/desktop/yt_1200.png" alt="YouTube Logo" id="youtube-logo" width="100">
        <button class="button" id="subscribe-btn">Subscribe</button>
    </header>

    <div id="main-content">
        <div id="video-container">
            <iframe id="video" width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <button class="button" id="play-btn">Play Video</button>
    </div>

    <div id="form-container">
        <h2>Subscribe Form</h2>
        <form>
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name"><br><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email"><br><br>
            <input type="submit" value="Subscribe" class="button">
        </form>
    </div>

    <script>
        document.getElementById('play-btn').addEventListener('click', function() {
            const iframe = document.getElementById('video');
            const src = iframe.src;
            iframe.src = src + "?autoplay=1";
        });

        document.getElementById('youtube-logo').addEventListener('click', function() {
            window.open('https://www.youtube.com', '_blank');
        });

        document.getElementById('subscribe-btn').addEventListener('click', function() {
            document.getElementById('form-container').style.display = 'flex';
        });
    </script>
    
</body>
</html>
