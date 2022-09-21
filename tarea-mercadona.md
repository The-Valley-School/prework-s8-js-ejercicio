>[ENUNCIADO - Diseño 1](S8-recursos/enunciado-mercadona-1.pdf)

>[ENUNCIADO - Diseño 2](S8-recursos/encunciado-mercadona-2.pdf)

>[RECURSOS](S8-recursos/mercadona-recursos.zip)

--- 

- Array de objetos de productos:

```js
/*
    Base de datos de productos
*/

let productos = [
    {
        id: 1,
        nombre: 'Pera Conferencia',
        precio: 0.34,
        imagen: 'item1.jpeg'
    },
    {
        id: 2,
        nombre: 'Manzana Golden',
        precio: 0.36,
        imagen: 'item2.jpeg'
    },
    {
        id: 3,
        nombre: 'Uvas',
        precio: 2.60,
        imagen: 'item3.jpeg'
    },
    {
        id: 4,
        nombre: 'Banana',
        precio: 0.21,
        imagen: 'item4.jpeg'
    },
    {
        id: 5,
        nombre: 'Melón Galia',
        precio: 2.71,
        imagen: 'item5.jpeg'
    },
    {
        id: 6,
        nombre: 'Mandarina',
        precio: 0.36,
        imagen: 'item6.jpeg'
    },
    {
        id: 7,
        nombre: 'Piña',
        precio: 2.30,
        imagen: 'item7.jpeg'
    },
    {
        id: 8,
        nombre: 'Mango',
        precio: 1.23,
        imagen: 'item8.jpeg'
    }
    
    
    
];
```

A partir de aquí podríamos enfocarlo de la misma manera que el ejercicio de globo:

ESTRUCTURA, HEADER Y FOOTER

Creamos nuestra estructura y maquetamos el header y footer.

- Tenemos un header con una imagen y color de fondo

```css
/* Color de fondo del header */
background-color: #5BB289;
```

- El footer está dividido en cuatro columnas, una de logo y tres de enlaces

```css
/* Color de fondo del footer */
background-color: #F7F8F6;
```

MAIN, LISTA DE PRODUCTOS

Utilizaremos nuestros conocimientos en HTML y CSS para ir montando un listado de items que tengan foto, nombre, precio y botón:

```css
#C8C8C8; /* Color de los bordes */
#F9B42A; /* Color del fondo del botón */
#714000; /* Color de la letra del botón */
```

MAIN, CARRITO DE LA COMPRA

Estructuramos cada uno de los elementos del carrito de compta:

```css
maroon /* color del texto de unidades */
```

LISTADO DE PRODUCTOS DINÁMICOS / CARRITO DE LA COMPRA DINÁMICOS

Tips importantes:

- Buscar el elemento donde introduciremos cada item:

```js
document.getElementById();
```

- Crear cada uno de los elementos y añadirlos a su nodo padre:

```js
document.createElement();
elemento.appendChild(elementoHijo);
```

- Aplicar bien las clases y propiedades

```js
element.classList.add();
element.setAttribute();
```

- Trabajar con función anónima cuando queramos pasar argumentos en  el add event listener

```js
element.addEventListener('click', function() { functionToCall(i) });
```
