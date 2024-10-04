
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>домтк макса</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Добро пожаловать в домик макса!</h1>
        <div class="tabs">
            <button class="tab-button" onclick="openTab(event, 'what')">Что такое леопаниксы</button>
            <button class="tab-button" onclick="openTab(event, 'how')">Как получить леопаниксы</button>
        </div>

        <div id="what" class="tab-content">
            <p>Леопаниксы — это валюта нашего Telegram канала.</p>
        </div>

        <div id="how" class="tab-content">
            <p>Леопаниксы можно получить за конкурсы и лотереи в нашем Telegram канале.</p>
        </div>

        <div class="button-container">
            <a href="https://t.me/ulyaandmaksimka" target="_blank" class="telegram-button">Перейти в наш Telegram канал</a>
        </div>
    </div>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tabbuttons;
            tabcontent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            tabbuttons = document.getElementsByClassName("tab-button");
            for (i = 0; i < tabbuttons.length; i++) {
                tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
            }
            document.getElementById(tabName).style.display = "block";
            evt.currentTarget.className += " active";
        }

        // Показать первую вкладку по умолчанию
        document.getElementsByClassName("tab-button")[0].click();
    </script>
</body>
</html>
<style>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
}

.container {
    max-width: 800px;
    margin: 50px auto;
    background-color: #fff;
    padding: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h1 {
    text-align: center;
    color: #333;
}

.tabs {
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
}

.tab-button {
    background-color: #4CAF50;
    color: white;
    border: none;
    padding: 14px 20px;
    margin: 0 5px;
    cursor: pointer;
    border-radius: 5px;
    transition: background-color 0.3s;
}

.tab-button:hover {
    background-color: #45a049;
}

.tab-button.active {
    background-color: #2e7d32;
}

.tab-content {
    display: none;
    padding: 20px;
    border-top: 1px solid #ccc;
    text-align: center;
    color: #333;
    font-size: 18px;
}

.tab-content p {
    margin: 0;
}

.button-container {
    text-align: center;
    margin-top: 30px;
}

.telegram-button {
    display: inline-block;
    padding: 12px 25px;
    background-color: #0088cc;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    font-size: 16px;
    transition: background-color 0.3s;
}

.telegram-button:hover {
    background-color: #007bb5;
}
</style>
