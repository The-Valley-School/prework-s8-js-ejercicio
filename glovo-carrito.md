 Por último tenemos el carrito de compra. En esta ocasión tendremos que maquetar dos opciones:

- La opción de que el carrito esté vacío, en este caso saldrá una imagen y texto
- La opción de que el carrito tenga productos, lo cual saldrá un listado y un total

Creamos primero la estructura del carrito con el título:

```html
<aside class="cart custom-border">
    <p class="cart-title">Tu glovo</p>
    <!-- Cuando no hay producto -->
    <div class="cart-no-products">
    </div>
		    <!-- Cuando hay producto -->
    <div class="cart-products">
        <!-- Aquí van los productos agregados al carrito -->
    </div>
</aside>
```

CARRITO VACÍO

Agregamos la imagen, el texto y maquetamos:

```html
<div class="cart-no-products">
    <img class="no-products-img" src="./assets/sin-productos.png">
    <p class="no-products-text"> Todavía no has añadido ningún producto. Cuando lo hagas, ¡verás los productos aquí! </p>
</div>
```

```css
.cart-no-products{
  padding: 30px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap; /* Esta propiedad sirve para permitir que los elementos se coloquen en varias líneas */
}

.no-products-img{
  width: 200px;
  margin: 0 auto;
}

.no-products-text{
  text-align: center;
  color: #A09FA0;
  font-size: 18px;
}
```

Cuando estemos trabajando ya con JS para mostrar esta opción o la del listado, jugaremos con la propiedad display:none / display:flex para mostrar o no esta sección.

CARRITO CON ELEMENTOS

Tendremos un elemento por linea que contenga:

- Cantidad, en nuestro caso iremos añadiendo elementos y no agruparemos por productos iguales así que siempre será 1
- Nombre del producto
- Precio
- Botón de eliminar

```js
<div id="cartItems" class="cart-products">
	<div class="cart-item">
	        <p class="cart-item-quantity">2X</p>
	        <p class="cart-item-description">MacMenu Big Mac</p>
	        <p class="cart-item-price">8,10 €</p>
	        <button class="cart-item-btn">x</button>
	</div>
</div>
```

```css
.cart-products{
  margin-top: 20px;
}

.cart-item{
  display: flex;
  justify-content: end;
  align-items: center;
}

.cart-item-quantity{
  font-weight: bold;
  margin: 5px;
}

.cart-item-description{
  margin: 5px;
}

.cart-item-price{
  margin: 5px;
}

.cart-item-btn{
  border-radius: 50px;
  border:none;
  background-color: #EAABA7;
  color: #951D14;
  width: 30px;
  height: 30px;
  margin: 5px 0;
}

```

Quedaría únicamente el TOTAL de los productos introducidos en el carrito:

```html
<p class="cart-total">Total: 100.00€</p>
```

```css
.cart-total{
  padding: 15px;
  background-color: #FBC244;
  color: #fff;
  font-size: 20px;
  text-align: center;
  font-weight: bold;
}
```

Con esto ya habríamos terminado de maquetar la web, vamos ahora a darle dinamismo e interacción.
