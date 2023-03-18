
2. Modificar un atributo
```jsx
console.log(h1.getAttribute('class')); // Nos enseña que clase tienen nuestro h1
h1.setAttribute('class','rojo'); // Nos modifico el nombre de nuestro atributo de class
h1.classList.add('rojo'); // Nos agrega una clase
h1.classList.remove('verde');  // Nos elimina una clase
```
3. Modificar un input
```jsx
input.value = "456"; // Nos modifico el value de nuestro input
input.placeholder = "Texto de prueba"; // Nos modifico nuestro placeholder
```
> # 4. Eventos
```jsx
// onchange: Escucha cuando el usuario termino de ponerle informacion al input
<input onchange="console.log('Cambio el input')" id="calculo2" placeholder="Escribe algo aquí" />

//onclick: Escucha cuando le dan click al boton
<button id="btnCalcular" onclick="console.log('click dek btn')">Calcular</button>

// addEventListener: Nos ayuda a poner un escuchador de eventos ya no en html si no directamente en JS unicamente necesita dos argumentos.
// form: Es donde vamos a escuchar el evento
// submit: El nombre del evento
// sumarInputValues: Tarea de JS que queremos que realize cuando escuche el evento
form.addEventListener('submit', sumarInputValues)'
```
### Cuando queremos que nuestro codigo JS escuche un evento que pasa en nuestro codigo html como por ejemplo el click de un boton, el llenado de un cuestionario o de un input tenemos dos opciones. 
1. Ponerle en html el escuchador de eventos como por ejemplo el onchange o el onclick pero tendriamos que ponerles muchos escuchadores de evento*/
2. Podemos crear una funcion en js que realice todas las tareas que queremos que realice todos los botones de cierto tipo y simplemente se la incorporamos al boton que queremos que realice ese tipo de tareas como si fuera un tipo class
```jsx
//Ejemplo 1 del boton - mala idea
<button id="btnCalcular" onclick="console.log('click dek btn')">Calcular</button>

//Ejemplo 2 del boton - Buena idea
// 1. Creamos la funcion en JS de lo que queremos que realice nuestro boton
function btnOnClick(){
    console.log('Escuchando el evento del click');
    };
// 2. La funcion que creamos en JS se la incorporamos a nuestro o nuestros botones como si fuera un tipo class
<button id="btnCalcular" onclick="btnOnClick()">Calcular</button>
```
### Otro ejemplo para cuando queremos crear un evento
```jsx
// Creamos nuestras variables
const menuEmail = document.querySelector('.navbar-email');
const desktopMenu = document.querySelector('.desktop-menu');

// Creamos el evento del click y la funcion que queremos que realice al momento de escuchar el evento
menuEmail.addEventListener('click', toggleDesktopMenu);

// Creamos la funcion que queremos que realice
function toggleDesktopMenu(){
     desktopMenu.classList.toggle('inactive'); // toggle: Es como una palanca algo que queremos que realice cuando precionamos click y que tiene que hacer cuando volvemos a hacer click por ejemplo una barra de menu la quita y la pone en cada click
 }
```




















