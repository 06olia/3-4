<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Вгадай число</title>
    <script>
        function guessNumber() {
            const secretNumber = Math.floor(Math.random() * 100) + 1;
            let guess;
            do {
                guess = parseInt(prompt("Вгадайте число від 1 до 100:"));
                if (guess < secretNumber) {
                    alert("Загадане число більше");
                } else if (guess > secretNumber) {
                    alert("Загадане число менше");
                } else if (isNaN(guess)) {
                    alert("Будь ласка, введіть число!");
                }
            } while (guess !== secretNumber);
            alert(Вітаємо! Ви вгадали число!");
        }
    </script>
</head>
<body>
    <button onclick="guessNumber()">Почати гру</button>
</body>
</html>
