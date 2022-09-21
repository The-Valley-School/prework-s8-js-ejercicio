Como siempre, empezamos generando nuestro index.html genérico, vinculamos un archivo css y un archivo js. A su vez creamos la carpeta assets donde tenemos todos los recursos necesarios, en este caso las imágenes del proyecto.

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

De momento nos vamos a centrar en el HEADER, tenemos que introducir una imagen y darle el formato amarillo al fondo:

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
}.header {
  background-color: #FBC244;
  padding: 25px;
}

.logo {
  width: 100px;
  height: auto;
}
```

Aprovechamos también y dejamos maquetado el footer. Agruparemos cada columna y pondremos también el logo.

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
