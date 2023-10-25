<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora</title>
    <div class="teladetras">
        <div class="calculadora">
            <p id="solucao"></p>
            <style>
        
.teladetras{
    background-color: rgb(0, 1, 1);
    height: 100vh;
            color: rgb(94, 94, 239);
            font-family: Arial;
            
}
.calculadora{
    position: absolute;
    top: 25%;
            left: 40%;
            border-radius: 15px;
            padding: 15px;
            background-color: rgb(0, 1, 1);
}
.botao{
            width: 50px;
            height: 50px;
            font-size: 25px;
            cursor: pointer;
            margin: 3px;
            background-color: rgb(94, 94, 239);
}
#solucao{
            background-color: white;
            width: 200px;
            height: 30px;
            margin: 3px;
            font-size: 20px;
            color: black;
            text-align: right;
            padding: 5px;
}
                </style>
            <table>
       <tr>
            <td><button class="botao" onclick="clean()">C</button></td>
            <td><button class="botao" onclick="back()">></button></td>
            <td><button class="botao" onclick="insert('/')">/</button></td>
            <td><button class="botao" onclick="insert('*')">X</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('7')">7</button></td>
            <td><button class="botao" onclick="insert('8')">8</button></td>
            <td><button class="botao" onclick="insert('9')">9</button></td>
            <td><button class="botao" onclick="insert('-')">-</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('4')">4</button></td>
            <td><button class="botao" onclick="insert('5')">5</button></td>
            <td><button class="botao" onclick="insert('6')">6</button></td>
            <td><button class="botao" onclick="insert('+')">+</button></td>
        </tr>
        <tr>
            <td><button class="botao" onclick="insert('1')">1</button></td>
            <td><button class="botao" onclick="insert('2')">2</button></td>
            <td><button class="botao" onclick="insert('3')">3</button></td>
            <td rowspan="2"><button class="botao" style="height: 106px;" onclick="calcular()">=</button></td>
        </tr>
        <tr>
            <td colspan="2"><button class="botao" style="width: 106px;" onclick="insert('0')">0</button></td>
            <td><button class="botao" onclick="insert('.')">.</button></td>
        </tr>
    </table>
</div>
</div>
<script>
function insert(num)
{
    var numero = document.getElementById('solucao').innerHTML;
    document.getElementById('solucao').innerHTML = numero + num;
}
function clean()
{
    document.getElementById('solucao').innerHTML = "";
}
function back()
{
    var resultado = document.getElementById('solucao').innerHTML;
    document.getElementById('solucao').innerHTML = resultado.substring(0, resultado.length -1);
}
function calcular()
{
    var resultado = document.getElementById('solucao').innerHTML;
    if(resultado)
    {
        document.getElementById('solucao').innerHTML = eval(resultado);
    }
    else
    {
        document.getElementById('solucao').innerHTML = "";
    }
}
</script>
</body>
</html>
