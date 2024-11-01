<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Образовательная платформа ОИС</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Образовательная платформа для студентов ОИС</h1>
        <nav>
            <ul>
                <li><a href="#courses">Курсы</a></li>
                <li><a href="#resources">Ресурсы</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="courses">
            <h2>Курсы</h2>
            <div class="course-card">
                <h3>Введение в информатику</h3>
                <p>Изучите основы информатики и программирования.</p>
                <button onclick="enrollCourse('Введение в информатику')">Записаться</button>
            </div>
            <div class="course-card">
                <h3>Системное программирование</h3>
                <p>Углубленное изучение системного программирования и разработки ПО.</p>
                <button onclick="enrollCourse('Системное программирование')">Записаться</button>
            </div>
        </section>

        <section id="resources">
            <h2>Ресурсы</h2>
            <ul>
                <li><a href="#">Учебники</a></li>
                <li><a href="#">Видеоуроки</a></li>
                <li><a href="#">Форумы</a></li>
            </ul>
        </section>
    </main>

    <footer>
        <section id="contact">
            <h2>Контакты</h2>
            <p>Связь с администрацией: <a href="mailto:admin@education-platform.com">admin@education-platform.com</a></p>
        </section>
        <p>&copy; 2023 Образовательная платформа ОИС</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
