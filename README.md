<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>НайдиЛекарство.kz - Поиск препаратов и консультация</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        .header {
            background-color: #e53935;
            color: white;
            padding: 20px;
            text-align: center;
        }
        .header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        .container {
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            color: #e53935;
        }
        input, button {
            width: 100%;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
            font-size: 1em;
        }
        input:focus {
            border-color: #e53935;
            outline: none;
        }
        button {
            background-color: #e53935;
            color: white;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #d32f2f;
        }
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 10px;
            background-color: #e53935;
            color: white;
        }
    </style>
</head>
<body>

    <!-- Шапка сайта -->
    <div class="header">
        <h1>НайдиЛекарство.kz</h1>
        <p>Поиск препаратов и консультации</p>
    </div>

    <!-- Основной контент -->
    <div class="container">
        <h2>Найдите нужный препарат</h2>
        
        <!-- Строка для поиска препарата -->
        <input type="text" id="medicationInput" placeholder="Введите название препарата">
        <button onclick="searchMedication()">Найти препарат</button>

        <h2>Консультация с фармацевтом</h2>

        <!-- Строка для консультации -->
        <input type="text" id="consultationInput" placeholder="Введите вопрос для фармацевта">
        <button onclick="consultPharmacist()">Отправить вопрос</button>
    </div>

    <!-- Подвал -->
    <footer>
        &copy; 2024 НайдиЛекарство.kz - Все права защищены.
    </footer>

    <script>
        // Функция для поиска препарата и отправки сообщения в WhatsApp
        function searchMedication() {
            var medication = document.getElementById("medicationInput").value;
            if (medication) {
                var url = "https://wa.me/+7771403909?text=Я%20ищу%20препарат:%20" + encodeURIComponent(medication);
                window.open(url, '_blank');
            } else {
                alert("Введите название препарата!");
            }
        }

        // Функция для отправки вопроса фармацевту через WhatsApp
        function consultPharmacist() {
            var question = document.getElementById("consultationInput").value;
            if (question) {
                var url = "https://wa.me/77001234567?text=Вопрос%20для%20фармацевта:%20" + encodeURIComponent(question);
                window.open(url, '_blank');
            } else {
                alert("Введите ваш вопрос!");
            }
        }
    </script>
</body>
</html>
