<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <title>Relógio</title>
</head>

<body>
    <div class="relogio">
        <div>
            <span id="horas">00</span>
            <span class="tempo">Horas</span>
        </div>

        <div>
            <span id="minutos">00</span>
            <span class="tempo">Minutos</span>
        </div>

        <div>
            <span id="segundos">00</span>
            <span class="tempo">Segundos</span>
        </div>
            <style>
            * {
                margin: 0;
                padding: 0;
            }
            
            body {
                height: 100vh;
                background-color: wheat;
                display: flex;
                align-items: center;
                justify-content: center;
            }
            
            .relogio {
                display: flex;
                align-items: center;
                justify-content: space-around;
                height: 200px;
                width: 500px;
            }
            
            .relogio div {
                height: 170px;
                width: 150px;
                display: flex;
                flex-direction: column;
                align-items: center;
                box-shadow: inset;
                justify-content: center;
                color: white;
                background: rgba(5, 5, 5, 0.829);
                letter-spacing: 4px;
            }
            
            .relogio span {
                font-weight: bolder;
                font-size: 66px;
            }
            
            .relogio span.tempo {
                font-size: 12px;
            }
            </style>   
    </div>
<script>

    const horas = document.getElementById('horas');
const minutos = document.getElementById('minutos');
const segundos = document.getElementById('segundos');

const relogio = setInterval(function time() {
    let dateToday = new Date();
    let hr = dateToday.getHours();
    let min = dateToday.getMinutes();
    let s = dateToday.getSeconds();

    if (hr < 10) hr = '0' + hr;

    if (min < 10) min = '0' + min;

    if (s < 10) s = '0' + s;

    horas.textContent = hr;
    minutos.textContent = min;
    segundos.textContent = s;

})
</script>
</body>
</html>
