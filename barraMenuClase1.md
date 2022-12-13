- Esta barra es como un pequeño menu que se nos aparece en la parte superior al darle click a nuestro menu amburguesa
```jsx
// Barra de navegacio
<div class="navbar-right">
      <ul>
        <li class="navbar-email">platzi@example.com</li>
        <li class="navbar-shopping-cart">
          <img src="./icons/icon_shopping_cart.svg" alt="shopping cart">
          <div>2</div>
        </li>
      </ul>
    </div>
    
    ![image](https://user-images.githubusercontent.com/66334502/207331655-13d9dc22-5049-4719-9a46-d85cf2373aef.png)

    
// Barra de menu
<div class="desktop-menu inactive">
        <ul>
          <li>
            <a href="/" class="title">My orders</a>
          </li>
    
          <li>
            <a href="/">My account</a>
          </li>
    
          <li>
            <a href="/">Sign out</a>
          </li>
        </ul>
      </div>
```
- Este es nuestro codigo JS que usamos para que aparesca o desaparesca al momento de darle click
```jsx
const menuEvamil = document.querySelector('.navbar-email');
const desktopMenu = document.querySelector('.desktop-menu');

menuEvamil.addEventListener('click', toggleDesktopMenu);

function toggleDesktopMenu(){
    desktopMenu.classList.toggle('inactive'); // Toggle te ayuda cuando quieres que algo aparesca y desaparesca con un click
}
```
