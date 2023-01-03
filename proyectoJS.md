- ## Barra de navegacion ( Escuchar eventos )
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
    

    
// Barra de menu que queremos que este apareciendo
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
- ## Crear la lista de productos
- Codigo de html esto es lo que se vera en nuestro codigo html
```html
<section class="main-container">
    <div class="cards-container">

</section>
```
- Codigo JS. Esto es lo que se va a ver en nuestro codigo JS
```jsx
/* Creando la lista de productos de nuestra pagina */

const productList = [];
productList.push({
  name: 'Bike', 
  price: '120',
  image: 'https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
});
productList.push({
  name: 'Pantalla', 
  price: '220',
  image: 'https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
});
productList.push({
  name: 'Compu', 
  price: '320',
  image: 'https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940'
});

/*Se crea la lista de productos para que se puedan meter automaticamente */
/* Este sera el codigo html que queremos sustituir por JS
<div class="product-card">
  <img src="https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="">
    <div class="product-info">
      <div>
        <p>$120,00</p>
        <p>Bike</p>
      </div>
      <figure>
        <img src="./icons/bt_add_to_cart.svg" alt="">
      </figure>
    </div>
</div> 
*/


for(product of productList) {
/*Se crea el div*/
  const productCard = document.createElement('div');
  productCard.classList.add('product-card');

/*Se crea la imagen*/
  const productImg = document.createElement('img');
  productImg.setAttribute('src', product.image);

/*Se crea otro div*/
  const productInfo = document.createElement('div');
  productInfo.classList.add('product-info');

/* Se agrega nuestro div en productInfoDiv*/
  const productInfoDiv = document.createElement('div');
  
/* Se crean dos parrados y e agregan a productInfoDiv*/
  
  const productPrice = document.createElement('p');
  productPrice.innerText = '$' + product.price;
  const productName = document.createElement('p');
  productName.innerText = product.name;

  productInfoDiv.appendChild(productPrice);
  productInfoDiv.appendChild(productName);


  const productInfoFigure = document.createElement('figure');
  const productImgCart = document.createElement('img');
  productImgCart.setAttribute('src', './icons/bt_add_to_cart.svg');

  productInfoFigure.appendChild(productImgCart);

  productInfo.appendChild(productInfoDiv);
  productInfo.appendChild(productInfoFigure);

  productCard.appendChild(productImg);
  productCard.appendChild(productInfo);

  cardsContainer.appendChild(productCard);
}
```




















