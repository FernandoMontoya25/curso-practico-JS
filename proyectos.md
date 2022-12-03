## Calculadora modo principiante utilizando metodos JS
> Codigo html
```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manipulación del DOM básica - Curso Práctico de JavaScript</title>
</head>
<body>
    <h1>Manipulación del DOM básica</h1>

    <input id="calculo1" placeholder="Escribe algo aquí" />
    <input id="calculo2" placeholder="Escribe algo aquí" />
    <!-- <button id="btnCalcular" onclick="btnOnClick()">Calcular</button> -->
    <button id="opSuma" onclick="sum()">Suma</button>
    <button id="opResta" onclick="rest()">Resta</button>
    <button id="opMultiplicacion" onclick="mult()">Multiplicacion</button>
    <button id="opDivicion" onclick="div()">Divicion</button>
    <p id="result"></p>
    <script src="./script.js"></script>
    
</body>
</html>
```
> Codigo JavaSCript
```jsx
const h1 = document.querySelector('h1');
const input1 = document.querySelector('#calculo1');
const input2 = document.querySelector('#calculo2');
const btn = document.querySelector('#btnCalcular');
const pResult = document.querySelector('#result');
const suma = document.querySelector('#suma');
const resta = document.querySelector('#resta');
const multiplicacion = document.querySelector('#multiplicacion');
const divicion = document.querySelector('#divicion');
const opSuma = document.querySelector('#opSuma')
const opResta = document.querySelector('#opResta')
const opMultiplicacion = document.querySelector('#opMultiplicacion')
const opDivicion = document.querySelector('#opDivicion')




function mult(){
    var multiplicacion = ((Number(input1.value) * Number(input2.value)));
    pResult.innerText = "Resultado " + multiplicacion;
};
function sum(){
    var suma = ((Number(input1.value) + Number(input2.value)));
    pResult.innerText = "Resultado " + suma;
};
function rest(){
    var resta = ((Number(input1.value) - Number(input2.value)));
    pResult.innerText = "Resultado " + resta;
};
function div(){
    var divicion = ((Number(input1.value) / Number(input2.value)));
    pResult.innerText = "Resultado " + divicion;
};

function btnOnClick(){ 
    var sumaInputs = ((Number(input1.value) + Number(input2.value)));
    pResult.innerText = "Resultado " + sumaInputs
};
```
