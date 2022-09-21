Lo primero que hacemos en el carrito es crear el listado en función del array que tenemos con los productos añadidos:

```js
let elementCartList = document.getElementById('cartItems');
```

```js
let elementCartItem = document.createElement('div');
for( let i = 0; i < cartItems.length; i++){
    let elementCartItem = document.createElement('div');
    elementCartItem.classList.add('cart-item');

    let elementCartQuantity = document.createElement('p');
    elementCartQuantity.classList.add('cart-item-quantity');
    elementCartQuantity.textContent = '1X';

    let elementCartDescription = document.createElement('p');
    elementCartDescription.classList.add('cart-item-description');
    elementCartDescription.textContent = cartItems[i].nombre;

    let elementCartPrice = document.createElement('p');
    elementCartPrice.classList.add('cart-item-price');
    elementCartPrice.textContent = cartItems[i].precio + '€';

    let elementItemBtn = document.createElement('button');
    elementItemBtn.classList.add('cart-item-btn');
    elementItemBtn.textContent = '-';
    elementItemBtn.addEventListener('click', function() { deleteProductFromCart(i) });
    
    elementCartItem.appendChild(elementCartQuantity);
    elementCartItem.appendChild(elementCartDescription);
    elementCartItem.appendChild(elementCartPrice);
    elementCartItem.appendChild(elementItemBtn);

    elementCartList.appendChild(elementCartItem);
    console.log(cartItems[i].precio);           
 }

```

La lógica que usaremos para renderizar el carrito es borrarlo todo y repintarlo cada vez que añadimos un producto. Usamos este truco: 

```js
elementCartList.textContent = ''; /* Truki para eliminar contenido dentro del div */
```

Añadimos también una variable para guardar el contenido de la suma de los productos y pintamos.

```js
totalPrice += cartItems[i].precio;
```

```js
let elementTotal = document.createElement('p');
        elementTotal.classList.add('cart-total');
        elementTotal.textContent = 'Total: ' + totalPrice.toFixed(2) + '€';

        elementCartList.appendChild(elementTotal);
```

Quedaría incluir una validación que nos muestre la imagen cuando no tengamos productos, quedando:

```js
function renderCart(){
    let elementNoCartList = document.getElementById('cartNoItems');

    let elementCartList = document.getElementById('cartItems');
    elementCartList.textContent = ''; /* Truki para eliminar contenido dentro del div */

    let totalPrice = 0;
    //comprobamos el estado del carrito, si no tiene items pintamos el dibujo de carrito vacío
    if(cartItems.length > 0){
        //eliminaremos la información de que no hay nada en el carro
        elementNoCartList.style.display = 'none';

        //pintaremos la lista
        for( let i = 0; i < cartItems.length; i++){
            let elementCartItem = document.createElement('div');
            elementCartItem.classList.add('cart-item');

            let elementCartQuantity = document.createElement('p');
            elementCartQuantity.classList.add('cart-item-quantity');
            elementCartQuantity.textContent = '1X';

            let elementCartDescription = document.createElement('p');
            elementCartDescription.classList.add('cart-item-description');
            elementCartDescription.textContent = cartItems[i].nombre;

            let elementCartPrice = document.createElement('p');
            elementCartPrice.classList.add('cart-item-price');
            elementCartPrice.textContent = cartItems[i].precio + '€';

            let elementItemBtn = document.createElement('button');
            elementItemBtn.classList.add('cart-item-btn');
            elementItemBtn.textContent = '-';
            elementItemBtn.addEventListener('click', function() { deleteProductFromCart(i) });
            
            elementCartItem.appendChild(elementCartQuantity);
            elementCartItem.appendChild(elementCartDescription);
            elementCartItem.appendChild(elementCartPrice);
            elementCartItem.appendChild(elementItemBtn);

            elementCartList.appendChild(elementCartItem);
            console.log(cartItems[i].precio);
            totalPrice += cartItems[i].precio;            
        }

        let elementTotal = document.createElement('p');
        elementTotal.classList.add('cart-total');
        elementTotal.textContent = 'Total: ' + totalPrice.toFixed(2) + '€';

        elementCartList.appendChild(elementTotal);

    } else {
        //mostraremos información de que no hay nada en el carro
        elementNoCartList.style.display = 'flex';
    }
}
```

Y para finalizar nuestro proyecto. Desarrollamos la lógica de eliminar un producto.

Como de momento sabemos trabajar únicamente con los métodos pop y push. Vamos a crearnos un listado auxiliar donde metamos todos los productos menos el que queremos eliminar.

```js
function deleteProductFromCart(elementPosition){
    let cartItemsAux = [];

    for(let i = 0; i< cartItems.length; i++){
        if(i !== elementPosition){
            cartItemsAux.push(cartItems[i]);
        }
    }
    cartItems = cartItemsAux;
    renderCart();
}
```

Y ya tendríamos nuestra página de Glovo ¡TERMINADA!
