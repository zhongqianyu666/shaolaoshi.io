# shaolaoshi.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>祝邵老师生日快乐！</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            font-family: 'Microsoft YaHei', sans-serif;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            text-align: center;
        }
        
        .container {
            position: relative;
            z-index: 10;
        }
        
        h1 {
            color: #d23669;
            font-size: 3rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            margin-bottom: 30px;
            animation: pulse 1.5s infinite alternate;
        }
        
        .message {
            background-color: rgba(255,255,255,0.8);
            padding: 20px;
            border-radius: 15px;
            max-width: 600px;
            margin: 0 auto 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .cake {
            position: relative;
            width: 200px;
            height: 120px;
            margin: 40px auto;
        }
        
        .plate {
            width: 220px;
            height: 20px;
            background: #f5f5f5;
            border-radius: 50%;
            position: absolute;
            bottom: -10px;
            left: -10px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }
        
        .layer {
            position: absolute;
            width: 200px;
            height: 40px;
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        .layer.bottom {
            bottom: 10px;
            background: #ffdfd3;
        }
        
        .layer.middle {
            bottom: 50px;
            background: #f8c8dc;
            width: 180px;
            left: 10px;
        }
        
        .layer.top {
            bottom: 90px;
            background: #fff;
            width: 160px;
            left: 20px;
            height: 30px;
        }
        
        .candle {
            position: absolute;
            width: 6px;
            height: 30px;
            background: #fff;
            bottom: 120px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 20;
        }
        
        .flame {
            position: absolute;
            width: 12px;
            height: 20px;
            background: #ffde59;
            border-radius: 50% 50% 20% 20%;
            bottom: 150px;
            left: 50%;
            transform: translateX(-50%);
            animation: flicker 0.5s infinite alternate;
            box-shadow: 0 0 10px #ffde59, 0 0 20px #ff914d;
            z-index: 30;
        }
        
        .decoration {
            position: absolute;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: #ff9ff3;
            box-shadow: 0 0 5px rgba(255,159,243,0.8);
        }
        
        .confetti {
            position: absolute;
            width: 10px;
            height: 10px;
            background: #feca57;
            opacity: 0;
        }
        
        .signature {
            margin-top: 30px;
            font-style: italic;
            color: #576574;
        }
        
        @keyframes pulse {
            from { transform: scale(1); }
            to { transform: scale(1.05); }
        }
        
        @keyframes flicker {
            0%, 100% { transform: translateX(-50%) scale(1); }
            50% { transform: translateX(-50%) scale(1.1) translateY(-2px); }
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); }
            100% { transform: translateY(-100vh) rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎉 祝邵老师生日快乐！ 🎉</h1>
        
        <div class="message">
            <p>亲爱的邵老师：</p>
            <p>在您生日的这一天，我们想送上最真挚的祝福！</p>
            <p>感谢您一直以来的辛勤付出和谆谆教诲，</p>
            <p>愿您新的一岁身体健康，工作顺利，生活幸福！</p>
            <p>🎂 生日快乐！ 🎂</p>
        </div>
        
        <div class="cake">
            <div class="plate"></div>
            <div class="layer bottom"></div>
            <div class="layer middle"></div>
            <div class="layer top"></div>
            <div class="candle"></div>
            <div class="flame"></div>
            
            <!-- 蛋糕装饰 -->
            <div class="decoration" style="top: 30px; left: 30px; background: #1dd1a1;"></div>
            <div class="decoration" style="top: 20px; right: 40px; background: #ff9ff3;"></div>
            <div class="decoration" style="top: 50px; left: 50px; background: #feca57;"></div>
            <div class="decoration" style="top: 60px; right: 30px; background: #5f27cd;"></div>
        </div>
        
        <p class="signature">—— 您的学生们敬上</p>
    </div>

    <script>
        // 创建彩色纸屑效果
        function createConfetti() {
            const colors = ['#feca57', '#ff6b6b', '#48dbfb', '#1dd1a1', '#f368e0', '#5f27cd'];
            
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.opacity = '1';
                confetti.style.animation = `float ${Math.random() * 3 + 2}s linear forwards`;
                confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                
                document.body.appendChild(confetti);
                
                // 移除纸屑元素
                setTimeout(() => {
                    confetti.remove();
                }, 5000);
            }
        }
        
        // 每隔一段时间创建纸屑
        setInterval(createConfetti, 300);
        
        // 初始创建一批纸屑
        for (let i = 0; i < 30; i++) {
            setTimeout(createConfetti, i * 100);
        }
        
        // 点击页面任何地方都会创建纸屑
        document.addEventListener('click', createConfetti);
    </script>
</body>
</html>
