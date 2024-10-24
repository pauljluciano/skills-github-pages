---
title: Welcome to my blog
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Maker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 50px;
        }
        h1 {
            color: #333;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
        }
        button:hover {
            background-color: #0056b3;
        }
        #password {
            margin-top: 20px;
            font-size: 24px;
            color: #007bff;
        }
    </style>
</head>
<body>

<h1>Password Maker</h1>
<p>Generate a strong password with just one click!</p>
<button onclick="generatePassword()">Generate Password</button>
<div id="password"></div>

<script>
    function generatePassword() {
        const length = 16; // Length of the password
        const charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()_+";
        let password = "";
        
        for (let i = 0; i < length; i++) {
            const randomIndex = Math.floor(Math.random() * charset.length);
            password += charset[randomIndex];
        }
        
        document.getElementById("password").innerText = password;
    }
</script>

</body>
</html>

