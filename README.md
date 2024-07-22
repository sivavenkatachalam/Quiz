<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .quiz-container {
            background-color: #e57acc;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            text-align: center;
            width: 50%;
            max-width: 600px;
            margin: auto;
        }

        h2 {
            margin-bottom: 20px;
        }

        .options {
            list-style-type: none;
            padding: 0;
            text-align: left;
        }

        .options li {
            padding: 10px;
            margin: 5px 0;
            background: #efefef;
            border-radius: 5px;
            cursor: pointer;
        }

        .options li.correct {
            background: #c8e6c9;
        }

        .options li.incorrect {
            background: #ffcdd2;
        }

    </style>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const options = document.querySelectorAll('.options li');
            const correctAnswer = 'D';

            options.forEach(option => {
                option.addEventListener('click', () => {
                    if (option.getAttribute('data-option') === correctAnswer) {
                        option.classList.add('correct');
                    } else {
                        option.classList.add('incorrect');
                    }
                });
            });
        });
    </script>
</head>
<body>
    <div class="quiz-container">
        <h2>In web design, what does CSS stand for?</h2>
        <ul class="options">
            <li data-option="A">A. Counter Strike: Source</li>
            <li data-option="B">B. Corrective Style Sheet</li>
            <li data-option="C">C. Computer Style Sheet</li>
            <li data-option="D">D. Cascading Style Sheet</li>
        </ul>
    </div>
</body>
</html>
