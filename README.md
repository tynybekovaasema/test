<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Тест: Бюджет, SWOT-анализ и логика</title>
    <style>
        body { font-family: Arial, sans-serif; background: #f4f4f4; text-align: center; }
        .container { width: 60%; margin: auto; background: white; padding: 20px; border-radius: 10px; }
        .question { margin: 10px 0; text-align: left; }
        button { padding: 10px 20px; background: blue; color: white; border: none; cursor: pointer; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Тест: Бюджет, SWOT-анализ и логика</h1>
        <form id="quiz-form">
            <h2>Часть 1: Бюджет и SWOT-анализ</h2>
            <div class="question">
                <p>1. Какая главная цель составления бюджета?</p>
                <label><input type="radio" name="q1" value="a"> Контроль и управление финансами</label>
                <label><input type="radio" name="q1" value="b"> Увеличение расходов</label>
                <label><input type="radio" name="q1" value="c"> Исключение налогов</label>
            </div>
            <div class="question">
                <p>2. Что представляет собой SWOT-анализ?</p>
                <label><input type="radio" name="q2" value="a"> Инструмент стратегического планирования</label>
                <label><input type="radio" name="q2" value="b"> Финансовый отчет</label>
                <label><input type="radio" name="q2" value="c"> Маркетинговая кампания</label>
            </div>
            <div class="question">
                <p>3. Какие факторы относятся к "угрозам" в SWOT-анализе?</p>
                <label><input type="radio" name="q3" value="a"> Новые конкуренты</label>
                <label><input type="radio" name="q3" value="b"> Уникальный продукт</label>
                <label><input type="radio" name="q3" value="c"> Высокая производительность</label>
            </div>
            <div class="question">
                <p>4. В чем отличие бюджета от финансового отчета?</p>
                <label><input type="radio" name="q4" value="a"> Бюджет - это прогноз, а отчет - факт</label>
                <label><input type="radio" name="q4" value="b"> Бюджет - это налоговый документ</label>
                <label><input type="radio" name="q4" value="c"> Разницы нет</label>
            </div>
            <div class="question">
                <p>5. Почему SWOT-анализ важен для бизнеса?</p>
                <label><input type="radio" name="q5" value="a"> Помогает принимать стратегические решения</label>
                <label><input type="radio" name="q5" value="b"> Определяет уровень прибыли</label>
                <label><input type="radio" name="q5" value="c"> Заменяет маркетинговый план</label>
            </div>
            <div class="question">
                <p>6. Какие аспекты входят в бюджет предприятия?</p>
                <label><input type="radio" name="q6" value="a"> Доходы, расходы, инвестиции</label>
                <label><input type="radio" name="q6" value="b"> Только расходы</label>
                <label><input type="radio" name="q6" value="c"> Только зарплаты</label>
            </div>
            <div class="question">
                <p>7. Какой SWOT-фактор можно контролировать?</p>
                <label><input type="radio" name="q7" value="a"> Сильные и слабые стороны</label>
                <label><input type="radio" name="q7" value="b"> Возможности</label>
                <label><input type="radio" name="q7" value="c"> Угрозы</label>
            </div>
            <div class="question">
                <p>8. Какой главный недостаток SWOT-анализа?</p>
                <label><input type="radio" name="q8" value="a"> Субъективность оценки</label>
                <label><input type="radio" name="q8" value="b"> Высокая стоимость</label>
                <label><input type="radio" name="q8" value="c"> Ограниченный срок действия</label>
            </div>
            <h2>Часть 2: Сложные логические задачи</h2>
            <div class="question">
                <p>9. У отца Петра три сына: Вася, Ваня и ...?</p>
                <label><input type="radio" name="q9" value="a"> Петр</label>
                <label><input type="radio" name="q9" value="b"> Иван</label>
                <label><input type="radio" name="q9" value="c"> Сергей</label>
            </div>
            <div class="question">
                <p>10. Какое число будет следующим в ряду: 2, 6, 12, 20, ...?</p>
                <label><input type="radio" name="q10" value="a"> 30</label>
                <label><input type="radio" name="q10" value="b"> 28</label>
                <label><input type="radio" name="q10" value="c"> 32</label>
            </div>
            <div class="question">
                <p>11. Один человек может построить дом за 10 дней. Сколько времени потребуется двум?</p>
                <label><input type="radio" name="q11" value="a"> 5 дней</label>
                <label><input type="radio" name="q11" value="b"> 10 дней</label>
                <label><input type="radio" name="q11" value="c"> 20 дней</label>
            </div>
            <div class="question">
                <p>12. Если 2+2=Fish, 3+3=Bird, то 4+4=?</p>
                <label><input type="radio" name="q12" value="a"> Dog</label>
                <label><input type="radio" name="q12" value="b"> Cat</label>
                <label><input type="radio" name="q12" value="c"> Tree</label>
            </div>
            <button type="button" onclick="checkAnswers()">Проверить результаты</button>
        </form>
        <p id="result"></p>
    </div>
    <script>
        function checkAnswers() {
            let correct = 0;
            let answers = ["a", "a", "a", "a", "a", "a", "a", "a", "a", "b", "a", "a"];
            for (let i = 1; i <= answers.length; i++) {
                let selected = document.querySelector(`input[name="q${i}"]:checked`);
                if (selected && selected.value === answers[i-1]) correct++;
            }
            document.getElementById("result").innerText = `Ваш результат: ${correct} из ${answers.length}`;
        }
    </script>
</body>
</html>
