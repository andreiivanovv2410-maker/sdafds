<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Автоматическое скачивание</title>
</head>
<body>
    <p>Начинаем скачивание файла...</p>
    
    <script>
        // Код, который сработает сразу после загрузки страницы
        window.onload = function() {
            // Укажите ссылку на файл (абсолютную или относительную)
            var fileUrl = "archive.zip"; 
            
            // Создаем скрытый элемент ссылки
            var link = document.createElement("a");
            link.href = fileUrl;
            link.download = "archive.zip"; // Атрибут, заставляющий браузер скачивать, а не открывать
            
            // Добавляем ссылку на страницу, кликаем по ней и сразу удаляем
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        };
    </script>
</body>
</html>
