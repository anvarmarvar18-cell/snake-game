<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Пенальти: Битва Легенд</title>
    <style>
        body { margin: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #2c3e50; color: white; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 100vh; overflow: hidden; }
        #scoreboard { display: flex; justify-content: space-between; width: 400px; padding: 10px 20px; background: rgba(0,0,0,0.8); border-radius: 10px; margin-bottom: 20px; font-size: 24px; font-weight: bold; }
        .score-box { text-align: center; }
        .score-box span { font-size: 14px; color: #aaa; display: block; }
        
        #game-container { position: relative; width: 600px; height: 400px; background: repeating-linear-gradient(0deg, #4caf50, #4caf50 50px, #45a049 50px, #45a049 100px); border: 4px solid white; border-bottom: none; border-radius: 10px 10px 0 0; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        
        /* Ворота */
        #goal { position: absolute; top: 20px; left: 100px; width: 400px; height: 150px; border: 5px solid white; border-bottom: none; background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20"><path d="M0 0l20 20M20 0L0 20" stroke="rgba(255,255,255,0.3)" stroke-width="1"/></svg>'); }
        
        /* Объекты на поле */
        #goalkeeper { position: absolute; bottom: 230px; left: 280px; font-size: 50px; transition: all 0.8s cubic-bezier(0.25, 1, 0.5, 1); z-index: 2; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }
        #ball { position: absolute; bottom: 50px; left: 280px; font-size: 40px; transition: all 0.6s cubic-bezier(0.25, 1, 0.5, 1); z-index: 3; }
        #kicker { position: absolute; bottom: 10px; left: 275px; font-size: 60px; z-index: 4; filter: drop-shadow(2px 4px 6px black); }
        
        /* Штрафная зона (линии) */
        .penalty-box { position: absolute; bottom: 0; left: 150px; width: 300px; height: 250px; border: 3px solid white; border-bottom: none; }
        .penalty-arc { position: absolute; bottom: 230px; left: 250px; width: 100px; height: 40px; border: 3px solid white; border-radius: 50px 50px 0 0; border-bottom: none; }
        .penalty-spot { position: absolute; bottom: 70px; left: 295px; width: 10px; height: 10px; background: white; border-radius: 50%; }

        /* Оверлеи выбора */
        .overlay { position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 10; display: none; }
        .overlay h2 { margin-bottom: 5px; color: #f1c40f; }
        .overlay p { color: #ccc; margin-bottom: 20px; }
        
        .grid-3x3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; width: 300px; }
        .grid-btn { padding: 20px; font-size: 16px; font-weight: bold; background: #34495e; color: white; border: 2px solid #2c3e50; border-radius: 8px; cursor: pointer; transition: 0.2s; }
        .grid-btn:hover { background: #3498db; transform: scale(1.05); }

        #message-board { position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); font-size: 40px; font-weight: bold; text-align: center; text-transform: uppercase; color: #fff; text-shadow: 2px 2px 10px #000; z-index: 5; display: none; width: 100%; }
        #next-btn { margin-top: 20px; padding: 10px 30px; font-size: 20px; background: #e74c3c; color: white; border: none; border-radius: 5px; cursor: pointer; display: none; z-index: 6; }
        #next-btn:hover { background: #c0392b; }
    </style>
</head>
<body>

    <div id="scoreboard">
        <div class="score-box"><span>Команда 1</span><div id="score1">0</div></div>
        <div class="score-box"><span>Раунд</span><div id="round-display">1</div></div>
        <div class="score-box"><span>Команда 2</span><div id="score2">0</div></div>
    </div>

    <div id="game-container">
        <!-- Поле и разметка -->
        <div class="penalty-arc"></div>
        <div class="penalty-box"></div>
        <div class="penalty-spot"></div>
        <div id="goal"></div>
        
        <!-- Игроки и мяч -->
        <div id="goalkeeper">🧤</div>
        <div id="ball">⚽</div>
        <div id="kicker">🧍‍♂️</div>

        <!-- Экран выбора -->
        <div id="selection-overlay" class="overlay">
            <h2 id="turn-title">Ход Игрока 1</h2>
            <p id="turn-desc">Второй игрок, отвернись! Выбери куда бить.</p>
            <div class="grid-3x3">
                <button class="grid-btn" onclick="makeChoice(1)">Лев Вер</button>
                <button class="grid-btn" onclick="makeChoice(2)">Цен Вер</button>
                <button class="grid-btn" onclick="makeChoice(3)">Прав Вер</button>
                <button class="grid-btn" onclick="makeChoice(4)">Лев Сре</button>
                <button class="grid-btn" onclick="makeChoice(5)">Цен Сре</button>
                <button class="grid-btn" onclick="makeChoice(6)">Прав Сре</button>
                <button class="grid-btn" onclick="makeChoice(7)">Лев Низ</button>
                <button class="grid-btn" onclick="makeChoice(8)">Цен Низ</button>
                <button class="grid-btn" onclick="makeChoice(9)">Прав Низ</button>
            </div>
        </div>

        <div id="message-board">ГОЛ!</div>
    </div>
    
    <button id="next-btn" onclick="resetForNextTurn()">Следующий удар</button>

    <script>
        let p1Score = 0;
        let p2Score = 0;
        let round = 1;
        let turnPhase = 1; // 1: Выбирает бьющий, 2: Выбирает вратарь, 3: Анимация
        let currentKicker = 1; // 1 = Команда 1 бьет, 2 = Команда 2 бьет
        
        let shotTarget = null;
        let saveTarget = null;

        // Координаты для 9 зон ворот (top/left для мяча и вратаря)
        // Вратарь стартует с bottom: 230px, left: 280px
        // Мяч летит в пределы сетки ворот (top: 20px до 170px, left: 100px до 500px)
        const zones = {
            1: { ballY: 30, ballX: 110, gkY: 200, gkX: 130 }, // Лево Верх
            2: { ballY: 30, ballX: 280, gkY: 200, gkX: 280 }, // Центр Верх
            3: { ballY: 30, ballX: 450, gkY: 200, gkX: 430 }, // Право Верх
            4: { ballY: 90, ballX: 110, gkY: 150, gkX: 120 }, // Лево Сред
            5: { ballY: 90, ballX: 280, gkY: 150, gkX: 280 }, // Центр Сред
            6: { ballY: 90, ballX: 450, gkY: 150, gkX: 440 }, // Право Сред
            7: { ballY: 140, ballX: 110, gkY: 80, gkX: 110 }, // Лево Низ
            8: { ballY: 140, ballX: 280, gkY: 80, gkX: 280 }, // Центр Низ
            9: { ballY: 140, ballX: 450, gkY: 80, gkX: 450 }  // Право Низ
        };

        const overlay = document.getElementById('selection-overlay');
        const turnTitle = document.getElementById('turn-title');
        const turnDesc = document.getElementById('turn-desc');
        const ball = document.getElementById('ball');
        const gk = document.getElementById('goalkeeper');
        const kickerIcon = document.getElementById('kicker');
        const msgBoard = document.getElementById('message-board');
        const nextBtn = document.getElementById('next-btn');

        function startGame() {
            startTurnPhase();
        }

        function startTurnPhase() {
            overlay.style.display = 'flex';
            msgBoard.style.display = 'none';
            nextBtn.style.display = 'none';
            
            if (turnPhase === 1) {
                turnTitle.innerText = `Игрок ${currentKicker} БЬЕТ (Месси/Роналду)`;
                turnDesc.innerText = `Игрок ${currentKicker === 1 ? 2 : 1}, отвернись! Выбери, куда направить мяч.`;
                kickerIcon.style.transform = "rotate(0deg) scale(1)";
            } else if (turnPhase === 2) {
                turnTitle.innerText = `Игрок ${currentKicker === 1 ? 2 : 1} НА ВОРОТАХ (Буффон/Нойер)`;
                turnDesc.innerText = `Игрок ${currentKicker}, отвернись! Выбери, куда прыгнуть.`;
            }
        }

        function makeChoice(zoneId) {
            if (turnPhase === 1) {
                shotTarget = zoneId;
                turnPhase = 2;
                startTurnPhase();
            } else if (turnPhase === 2) {
                saveTarget = zoneId;
                turnPhase = 3;
                overlay.style.display = 'none';
                playAnimation();
            }
        }

        function playAnimation() {
            // Анимация замаха бьющего
            kickerIcon.style.transform = "rotate(-15deg) scale(1.1)";
            
            setTimeout(() => {
                kickerIcon.style.transform = "rotate(10deg) scale(0.9)";
                
                // Мяч летит в выбранную точку
                ball.style.top = zones[shotTarget].ballY + 'px';
                ball.style.left = zones[shotTarget].ballX + 'px';
                ball.style.transform = "rotate(720deg) scale(0.6)";

                // Вратарь прыгает
                // Если угадал, прыгает точно за мячом. Если нет - в выбранную им зону.
                let targetGkZone = saveTarget;
                gk.style.bottom = zones[targetGkZone].gkY + 'px';
                gk.style.left = zones[targetGkZone].gkX + 'px';
                
                // Наклон вратаря при прыжке
                if ([1, 4, 7].includes(targetGkZone)) gk.style.transform = "rotate(-60deg)";
                else if ([3, 6, 9].includes(targetGkZone)) gk.style.transform = "rotate(60deg)";
                else gk.style.transform = "scale(1.2)"; // Стоит по центру

                calculateResult();
            }, 500);
        }

        function calculateResult() {
            setTimeout(() => {
                let isGoal = true;
                
                // Система характеристик: 
                // Вратарь отбивает на 100%, если угадал точную зону.
                if (shotTarget === saveTarget) {
                    isGoal = false;
                }
                
                if (isGoal) {
                    msgBoard.innerText = "⚽ ГОЛ! Блестящий удар!";
                    msgBoard.style.color = "#2ecc71";
                    if (currentKicker === 1) p1Score++;
                    else p2Score++;
                } else {
                    msgBoard.innerText = "🧤 СЕЙВ! Невероятная реакция!";
                    msgBoard.style.color = "#e74c3c";
                    // Мяч отскакивает при сейве
                    ball.style.top = (zones[shotTarget].ballY + 50) + 'px';
                    ball.style.left = (zones[shotTarget].ballX - 50) + 'px';
                }

                document.getElementById('score1').innerText = p1Score;
                document.getElementById('score2').innerText = p2Score;
                msgBoard.style.display = 'block';
                nextBtn.style.display = 'block';
            }, 600); // Ждем окончания анимации мяча (0.6s)
        }

        function resetForNextTurn() {
            // Возвращаем объекты на исходные позиции
            ball.style.transition = "none";
            gk.style.transition = "none";
            kickerIcon.style.transition = "none";
            
            ball.style.top = "";
            ball.style.bottom = "50px";
            ball.style.left = "280px";
            ball.style.transform = "rotate(0deg) scale(1)";
            
            gk.style.bottom = "230px";
            gk.style.left = "280px";
            gk.style.transform = "rotate(0deg) scale(1)";
            
            kickerIcon.style.transform = "rotate(0deg) scale(1)";

            // Смена ролей
            if (currentKicker === 1) {
                currentKicker = 2; // Команда 2 теперь бьет
            } else {
                currentKicker = 1;
                round++; // Раунд завершен после 2 ударов
                document.getElementById('round-display').innerText = round;
            }

            turnPhase = 1;
            
            // Восстанавливаем плавность после сброса
            setTimeout(() => {
                ball.style.transition = "all 0.6s cubic-bezier(0.25, 1, 0.5, 1)";
                gk.style.transition = "all 0.8s cubic-bezier(0.25, 1, 0.5, 1)";
                kickerIcon.style.transition = "all 0.3s";
                startTurnPhase();
            }, 50);
        }

        // Запуск
        startGame();
    </script>
</body>
</html>
