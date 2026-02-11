<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mining App</title>
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
        body { background: #1a1a1a; color: white; text-align: center; font-family: sans-serif; }
        .coin { width: 200px; height: 200px; border-radius: 50%; background: gold; margin: 50px auto; 
                display: flex; align-items: center; justify-content: center; font-size: 50px;
                cursor: pointer; box-shadow: 0 0 20px yellow; transition: transform 0.1s; }
        .coin:active { transform: scale(0.9); }
        #balance { font-size: 24px; margin-top: 20px; }
    </style>
</head>
<body>
    <h1>عدّن الآن! ⛏️</h1>
    <div class="coin" id="mineBtn">💰</div>
    <div id="balance">رصيدك: 0</div>

    <script>
        const tg = window.Telegram.WebApp;
        tg.expand(); // لفتح الصفحة بكامل الشاشة

        let balance = 0;
        const btn = document.getElementById('mineBtn');
        const balDisplay = document.getElementById('balance');

        btn.onclick = () => {
            balance += 1;
            balDisplay.innerText = "رصيدك: " + balance;
            
            // إرسال البيانات للبوت عند الضغط (اختياري)
            // tg.sendData(balance.toString()); 
        };
    </script>
</body>
</html>
