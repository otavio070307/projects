<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ghost</title>
    <link rel="stylesheet" href="styles.css">
    <style>
body {
    margin: 0;
    padding: 0;
    background-color: #2c3456;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center
}
.ghost {
    width: 140px;
    height: 160px;
    background-color: #f2f2f2;
    border-radius: 70px 70px 0 0;
    position: relative;
    cursor: pointer;
    animation: floating 2s infinite ease-in-out;
}
@keyframes floating {
    50% {
        transform: translateY(-30px);
    }
}
.face {
    width: 100px;
    position: absolute;
    top: 60px;
    left: calc(50% - 50px);
}
.eyes {
    height: 24px;
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-bottom: 14px;
}
.eyes span {
    width: 24px;
    height: 24px;
    background-color: #2c3a47;
    border-radius: 50%;
    transition: .3s linear;
}
.ghost:hover .eyes span {
    height: 16px;
}
.mouth {
    width: 40px;
    height: 20px;
    background-color: #2c3a47;
    margin: auto;
    border-radius: 0 0 20px 20px;
    transition: .3s linear;
}
.ghost:hover .mouth {
    height: 12px;
}
.hands {
    width: 180px;
    position: absolute;
    left: -20px;
    top: 80px;
    display: flex;
    justify-content: space-between;
}
.hands span {
    width: 20px;
    height: 30px;
    background-color: #f2f2f2;
}
.hands span:first-child {
    border-radius: 20px 0 0 20px;
}
.hands span:last-child {
    border-radius: 0 20px 20px 0;
}
.feet {
    position: absolute;
    width: 100%;
    bottom: -20px;
    display: flex;
}
.feet span {
    flex: 1;
    height: 20px;
    background-color: #f2f2f2;
    border-radius: 0 0 20px 20px;
}
.feet span:first-child {
    border-radius: 0 0 20px 12px;
}
.feet span:last-child {
    border-radius: 0 0 12px 12px;
}
    </style>
</head>
<body>
    <div class="ghost">
        <div class="face">
            <div class="eyes">
                <span></span><span></span>
            </div>
            <div class="mouth"></div>
        </div>
        <div class="hands">
            <span></span><span></span>
        </div>

        <div class="feet">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
        </div>
    </div>
</body>
</html>
