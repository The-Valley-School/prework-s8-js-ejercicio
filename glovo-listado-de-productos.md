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
