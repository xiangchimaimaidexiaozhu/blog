---
title: 关于我
layout: page
---
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>正在跳转到 ForeverBlog</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            padding: 20px;
        }
        
        .container {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            max-width: 600px;
            width: 100%;
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .logo {
            font-size: 60px;
            margin-bottom: 20px;
            color: #ffdd40;
            animation: pulse 2s infinite;
        }
        
        h1 {
            font-size: 32px;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        p {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .countdown {
            font-size: 24px;
            font-weight: bold;
            margin: 25px 0;
            color: #ffdd40;
        }
        
        .progress-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 4px;
            margin: 30px 0;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            width: 0%;
            background: #ffdd40;
            border-radius: 4px;
            animation: progress 5s linear forwards;
        }
        
        .btn {
            display: inline-block;
            background: #ffdd40;
            color: #2c3e50;
            padding: 15px 35px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 18px;
            transition: all 0.3s ease;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .btn:hover {
            background: #ffd324;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .footer {
            margin-top: 40px;
            font-size: 14px;
            opacity: 0.7;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
        
        @keyframes progress {
            0% { width: 0%; }
            100% { width: 100%; }
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 30px 20px;
            }
            
            h1 {
                font-size: 26px;
            }
            
            p {
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">
            <i class="fas fa-blog"></i>
        </div>
        <h1>正在跳转到 ForeverBlog</h1>
        <p>您将在 <span id="countdown" class="countdown">1</span> 秒后自动跳转到 十年之约网站</p>
        
        <div class="progress-bar">
            <div class="progress"></div>
        </div>
        
        <p>如果跳转未发生，请点击下面的按钮手动访问</p>
        <a href="https://foreverblog.cn" class="btn">
            <i class="fas fa-external-link-alt"></i> 立即访问
        </a>
        
        <div class="footer">
            <p>© 2023 - ForeverBlog 精彩文章等着您</p>
        </div>
    </div>

    <script>
        // 倒计时和跳转功能
        let seconds = 1;
        const countdownElement = document.getElementById('countdown');
        
        const countdownInterval = setInterval(() => {
            seconds--;
            countdownElement.textContent = seconds;
            
            if (seconds <= 0) {
                clearInterval(countdownInterval);
                window.location.href = "https://foreverblog.cn";
            }
        }, 1000);
        
        // 5秒后自动跳转
        setTimeout(() => {
            window.location.href = "https://foreverblog.cn";
        }, 5000);
    </script>
</body>
</html>