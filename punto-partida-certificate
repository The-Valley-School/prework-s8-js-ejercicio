>[ENUNCIADO - Diseño 1](S8-recursos/enunciado-glovo-1.pdf)

>[ENUNCIADO - Diseño 2](S8-recursos/enunciado-glovo-2.pdf)

---

Bienvenidos a esta última sesión. Tras haber aprendido las nociones básicas de JS, vamos a realizar un ejercicio que va a englobar todo lo aprendido. Tras él, os dejaremos de tarea uno muy similar para que sigáis practicando.

¡Empezamos! En esta ocasión tenemos una página web de comida a domicilio, donde hay un listado de productos que podremos ir añadiendo al carrito de la compra.

El carrito de la compra a su vez irá añadiendo estos productos seleccionados y sumando el importe total a pagar.

Os vamos a dar el código HTML y CSS como punto de partida. 

- ESTRUCTURA

Empezamos generando nuestro index.html genérico, creando la estructura y vinculando un archivo css y un archivo js. A su vez creamos la carpeta assets donde tenemos todos los recursos necesarios, en este caso las imágenes del proyecto.

Analizando la estructura de la página web tendríamos 3 secciones:

- Sección HEADER donde tendremos el logo de Glovo con el fondo amarillo
- Sección que engloba el MAIN (lista de productos) y ASIDE (carrito de compra)
- Sección FOOTER

Creamos esta estructura principal:

```html
<!-- Primer Bloque: Header -->
<header>
</header>

<!-- Segundo Bloque: Contiene el listado de items y el carrito -->
<section>
    <main></main>
    <aside></aside>
</section>

<!-- Terce Bloque: Footer -->

<footer">
</footer>
```

- HEADER

Tenemos que introducir una imagen y darle el formato amarillo al fondo:

```html
<header class="header">
        <img class="logo" src="./assets/logo.png">
</header>
```

```css
/* GLOBAL STYLES */
body {
  background: #fff;
  color: #000;
  margin: 0;
  font-family: sans-serif;
}

/* HEADER */

.header {
  background-color: #FBC244;
  padding: 25px;
}

.logo {
  width: 100px;
  height: auto;
}
```

- Seguiremos con el FOOTER

Donde agruparemos cada columna y pondremos también el logo.

```html
<footer class="footer">
    <div class="footer-container">
        <img class="logo" src="./assets/logo-footer.png">
        <div class="footer-links">
            <div class="footer-links-column">
                <p class="footer-link-title">Colabora con Glovo</p>
                <a class="footer-link" href="#">Trabaja con nosotros</a>
                <a class="footer-link" href="#">Glovo para Partners</a>
                <a class="footer-link" href="#">Repartidores</a>
                <a class="footer-link" href="#">Glovo Business</a>
            </div>
            <div class="footer-links-column">
                <p class="footer-link-title">Enlaces de interés</p>
                <a class="footer-link" href="#">Acerca de nosotros</a>
                <a class="footer-link" href="#">Preguntas frecuentes</a>
                <a class="footer-link" href="#">Blog</a>
                <a class="footer-link" href="#">Contacto</a>
                <a class="footer-link" href="#">Seguridad</a>
            </div>
            <div class="footer-links-column">
                <p class="footer-link-title">Sígenos</p>
                <a class="footer-link" href="#">Facebook</a>
                <a class="footer-link" href="#">Twitter</a>
                <a class="footer-link" href="#">Instragram</a>
            </div>
        </div>
    </div>
</footer>
```

```css
.footer {
  background-color: #1D1D1C;
}

.footer-container{
  max-width: 1000px;
  margin: 0 auto; /* auto (pequeño truki para centrar) */
  padding: 40px 0;
}

.footer-links {
  display: flex;
  margin-top: 20px;
}

.footer-links-column {
  margin-right: 100px;
}

.footer-link-title{
  color: white;
  font-weight: bolder;
  font-size: 20px;
}

.footer-link {
  color: #A09FA0;
  text-decoration: none;
  font-size: 14px;
  font-weight: 100;
  margin-bottom: 15px;
  display: block; /* para que salgan cada uno en una linea */
}
```

- Maquetaremos el LISTADO DE PRODUCTOS

Vamos ahora con el listado de productos. De momento vamos a maquetarlo tal y como lo haríamos en una página estática aunque en siguientes videos veamos como crearlo dinámicamente con JS:

Tenemos el nombre del restaurante, el tiempo de entrega, el título del listado (Top Ventas) y una serie de items:

```html
<main class="main custom-border">
    <h2 class="restaurant-title">Mcdonald's</h2>
    <p class="restaurant-info">Tiempo de entrega: 15-20'</p>
    <h3 class="restaurant-items-title">Top ventas</h3>
    <div class="restaurant-items">
        <!-- Aquí van los items -->
    </div>
</main>
```

```css
.container{
  display: flex;
  align-items: flex-start; /* centramos en la parte superior */
  justify-content: center;
}

.main{
  width: 750px;
  margin: 20px 10px 20px 20px;
  padding: 40px;
}

.custom-border{
  box-shadow: 0 1px 5px rgb(0 0 0 / 15%); /* Nos sirve para darle esa sombra */
  border-radius: 8px;
}

.restaurant-title{
  font-size: 35px;
  margin: 0;
}

.restaurant-info{
  font-size: 14px;
  color: #A09FA0;
  padding-bottom: 20px;
  border-bottom: 2px solid #C8C8C8;
}

.restaurant-items-title{
  font-size: 22px;
  margin-top: 50px;
}
```

Cada Item, tiene a su vez:

- Una imagen
- Nombre del producto
- Precio del producto
- Botón de añadir al carrito

```html
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

```css
.item{
  border-radius: 10px;
  border: 1px solid #C8C8C8;
  padding: 15px;
  width: 300px;
  margin: 10px;
  display: inline-block;
}

.item-description{
  display: flex;
  align-items: flex-start;
  justify-content: left;
}

.item-order{
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.item-img{
  width: 100px;
}

.item-price{
  text-align: left;
}

.item-add{
  border-radius: 200px;
  border:none;
  background-color: #E8F8F5;
  color: #35A183;
  font-size: 25px;
  min-width: 30px;
}
```

- Maquetaremos por último el carrito de la compra para posteriormente empezar a aplicarle la lógica con JS. En esta ocasión tendremos que maquetar dos opciones:

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

### CARRITO VACÍO

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

### CARRITO CON ELEMENTOS

Tendremos un elemento por linea que contenga:

- Cantidad, en nuestro caso iremos añadiendo elementos y no agruparemos por productos iguales así que siempre será 1
- Nombre del producto
- Precio
- Botón de eliminar

```html
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

Con esto ya habríamos terminado de maquetar la web. Abajo tienes el código que te servirá como punto de partida para que puedas pasar directamente a lo importante, añadirle dinamismo e interacción.

>[PUNTO DE PARTIDA](S8-recursos/punto-partida-glovo.zip)

El ejercicio lo dividiremos en dos videos que nos permitirán ir incrementando el avance:

1. Crearemos de manera dinámica en función de un array de productos la sección de comida
2. Programaremos la lógica de añadir y quitar contenido del carrito

---

