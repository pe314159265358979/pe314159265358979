<!DOCTYPE html>
<html>
<head>
    <title>Прокси-сервер</title>
</head>
<body>
    <h1>Прокси-сервер</h1>
    <button onclick="sendRequest()">Отправить запрос</button>
    <div id="output"></div>

    <script>
        function sendRequest() {
            var proxyUrl = 'https://ww.fdsf.com/';
            var targetUrl = 'https://www.youtube.com/';
            fetch(proxyUrl + targetUrl)
                .then(response => response.text())
                .then(data => {
                    document.getElementById('output').innerHTML = data;
                })
                .catch(error => {
                    console.error('Ошибка:', error);
                });
        }
    </script>
</body>
</html>
