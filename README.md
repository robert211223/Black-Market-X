<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login cu Cheie</title>
    <style>
        /* Stiluri generale pentru tema întunecată */
        body {
            font-family: Arial, sans-serif;
            background-color: #121212; /* Fundal întunecat */
            color: #ffffff; /* Text alb */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .login-container {
            background-color: #1e1e1e; /* Container întunecat */
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.1); /* Umbra albă */
            width: 300px;
        }

        .login-container h2 {
            margin-bottom: 20px;
            font-size: 24px;
            text-align: center;
            color: #ffffff; /* Text alb */
        }

        .login-container input[type="text"],
        .login-container input[type="password"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #333; /* Bordură întunecată */
            border-radius: 4px;
            font-size: 16px;
            background-color: #333; /* Fundal câmp de text întunecat */
            color: #ffffff; /* Text alb */
        }

        .login-container input[type="text"]::placeholder,
        .login-container input[type="password"]::placeholder {
            color: #bbb; /* Culoare placeholder deschisă */
        }

        .login-container input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #28a745; /* Verde */
            border: none;
            border-radius: 4px;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
        }

        .login-container input[type="submit"]:hover {
            background-color: #218838; /* Verde mai închis la hover */
        }

        /* Opțional: Buton pentru schimbarea temei */
        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: #333;
            color: #fff;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="login-container">
    <h2>Login cu Cheie</h2>
    <form action="#" method="post">
        <label for="username">Utilizator:</label>
        <input type="text" id="username" name="username" placeholder="Introdu numele de utilizator" required>

        <label for="key">Cheie:</label>
        <input type="password" id="key" name="key" placeholder="Introdu cheia" required>

        <input type="submit" value="Login">
    </form>
</div>

<!-- Opțional: Buton pentru schimbarea temei -->
<button class="theme-toggle" onclick="toggleTheme()">Schimbă Tema</button>

<script>
    // Opțional: Funcție pentru schimbarea temei
    function toggleTheme() {
        const body = document.body;
        const container = document.querySelector('.login-container');
        const inputs = document.querySelectorAll('.login-container input');
        const button = document.querySelector('.theme-toggle');

        if (body.style.backgroundColor === 'rgb(18, 18, 18)') {
            // Tema deschisă
            body.style.backgroundColor = '#f4f4f4';
            body.style.color = '#000';
            container.style.backgroundColor = '#fff';
            container.style.boxShadow = '0 0 10px rgba(0, 0, 0, 0.1)';
            inputs.forEach(input => {
                input.style.backgroundColor = '#fff';
                input.style.color = '#000';
                input.style.borderColor = '#ccc';
            });
            button.textContent = 'Tema Întunecată';
        } else {
            // Tema întunecată
            body.style.backgroundColor = '#121212';
            body.style.color = '#fff';
            container.style.backgroundColor = '#1e1e1e';
            container.style.boxShadow = '0 0 10px rgba(255, 255, 255, 0.1)';
            inputs.forEach(input => {
                input.style.backgroundColor = '#333';
                input.style.color = '#fff';
                input.style.borderColor = '#333';
            });
            button.textContent = 'Tema Deschisă';
        }
    }
</script>

</body>
</html>
