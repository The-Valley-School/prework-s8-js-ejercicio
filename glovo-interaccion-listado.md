Vamos primero a crear de manera dinámica nuestro listado de productos. Partimos de la base de que tenemos el siguiente objeto:

```js
let productos = [
    {
        id: 1,
        nombre: 'Big Mac',
        precio: 8.15,
        imagen: 'item1.png'
    },
    {
        id: 2,
        nombre: 'American Chicken',
        precio: 9.35,
        imagen: 'item2.png'
    },
    {
        id: 3,
        nombre: 'Grand McExtreme',
        precio: 10.45,
        imagen: 'item3.png'
    },
    {
        id: 4,
        nombre: 'McMenu CBO',
        precio: 9.55,
        imagen: 'item4.png'
    },
    {
        id: 5,
        nombre: 'McNuggets',
        precio: 10.95,
        imagen: 'item5.png'
    },
    {
        id: 5,
        nombre: 'Alitas/McNuggets',
        precio: 11.25,
        imagen: 'item6.png'
    },
    {
        id: 6,
        nombre: 'McFlurry Oreo',
        precio: 33.55,
        imagen: 'item6.png'
    }
    
    
];
```

A partir de esto, crearemos una función que se inicie al cargar el script y recorra el array pintándolo en el DOM:

```js
function renderProducts(){
    for( let i = 0; i < productos.length; i++){
			// creamos elemento
		}
}
```

La estructura a pintar es: 

```js
<div class="item">
        <div class="item-description">
            <img class="item-img" src="./assets/item1.png">
            <p class="item-name">MacMenu Big Mac</p>
        </div>
        <div class="item-order">
            <p class="item-price">8,10 €</p>
            <button class="item-add">+</button>
        </div>
    </div>
```

Que utilizando lo aprendido en la sesión anterior se traduce a:

```js
function renderProducts(){
    let listElement = document.getElementById('listItems');

    for( let i = 0; i < productos.length; i++){

        let divElementItem = document.createElement('div');
        divElementItem.classList.add('item');

        let divElementItemDescription = document.createElement('div');
        divElementItemDescription.classList.add('item-description');

        let imgElementItem = document.createElement('img');
        imgElementItem.classList.add('item-img');
        let url = './assets/' + productos[i].imagen;
        imgElementItem.setAttribute('src', url);

        let nameElementItem = document.createElement('p');
        nameElementItem.classList.add('item-name');
        nameElementItem.textContent = productos[i].nombre;

        let divElementItemOrder = document.createElement('div');
        divElementItemOrder.classList.add('item-order');

        let priceElementItem = document.createElement('p');
        priceElementItem.classList.add('item-price');
        priceElementItem.textContent = productos[i].precio + '€';

        let buttonElementItem = document.createElement('button');
        buttonElementItem.classList.add('item-add');
        buttonElementItem.textContent = '+';
        buttonElementItem.addEventListener('click', function() { addProductsToCart(productos[i]) });

        divElementItemDescription.appendChild(imgElementItem);
        divElementItemDescription.appendChild(nameElementItem);
        
        divElementItemOrder.appendChild(priceElementItem);
        divElementItemOrder.appendChild(buttonElementItem);

        divElementItem.appendChild(divElementItemDescription);
        divElementItem.appendChild(divElementItemOrder);

        listElement.appendChild(divElementItem);
    }
}
```

Dejamos preparada también la interacción con el carrito:

```js
function addProductsToCart(item){
    cartItems.push(item); //añadimos al array un producto
    renderCart();         //renderizamos de nuevo todo el carrito
}
```
