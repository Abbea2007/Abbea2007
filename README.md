<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Heart Animation</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: black;
        }
        .heart {
            position: relative;
            width: 100px;
            height: 90px;
        }
        .heart::before,
        .heart::after {
            content: "";
            position: absolute;
            top: 0;
            width: 52px;
            height: 80px;
            background: red;
            border-radius: 50px 50px 0 0;
        }
        .heart::before {
            left: 50px;
            transform: rotate(-45deg);
            transform-origin: 0 100%;
        }
        .heart::after {
            left: 0;
            transform: rotate(45deg);
            transform-origin: 100% 100%;
        }
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
            100% {
                transform: scale(1);
            }
        }
        .heart {
            animation: pulse 1s infinite;
        }
    </style>
</head>
<body>
    <div class="heart"></div>
</body>
</html>
