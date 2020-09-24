# Module 2 - Lab: Creando Páginas HTML5 usando CSS3

>**Objetivos**: 
* El principal objetivo de este laboratorio es hacer usos de las los estilos CSS sobre las páginas htmls **Home** y **About**.
* Tener la destreza de construir una aplicación web simple con HTML5 que contengas páginas como **Home** u **About**.


### Lab Pasos

#### Ejercicio 1: Creando Páginas HTML5

#### Paso 1: Crear una aplicación web nueva ASP.NET

* Abrir Visual Studio 2019
* Crear un nuevo proyecto: **ContosoConf**.

#### Paso 2: Agregar una pagina index.html
* Agregar un header en la pagina
* Agregar una etiqueta section
```
    <section>
        <p>
            The web keeps evolving. There's a wealth of new technologies to keep up with! ContosoConf is an in-depth exploration of HTML5, CSS3, and JavaScript, in the heart of Seattle, WA.

        </p>
        <p>
            Don't miss the best speakers in the business, talking about the future of the web.
        </p>
    </section>
```
* Agregar otra etiqueta section
```html
    <section>
        <h2>Featuring these excellent speakers</h2>
        <ul>
            <li>Melissa Kerr</li>
            <li>David Alexander</li>
            <li>Mark Hanson</li>
            <li>April Meyer</li>
        </ul>
    </section>
```
* Agregar una tercera etiqueta section
```html
    <section>
        <h2>Thanks to our sponsors</h2>
        <ul>
            <li>Trey Research</li>
            <li>Litware, Inc</li>
            <li>Fourth Coffee</li>
            <li>Graphic Design Institute</li>
            <li>Southridge Video</li>
        </ul>
    </section>
```
* Agregar una etiqueta footer
```html
    <footer>
        <p>
            Hosted by Contoso
        </p>
        <address>
            Conference Center<br />
            3 Somewhere Street<br />
            Seattle<br />
            WA 98999
        </address>
        <p>
            &#169; 2012 Contoso
        </p>
    </footer>
```

#### Paso 3: Agregar imagenes a la página Home

* Crear la carpeta **images** en el proyecto
* En las páginas index y about sustituir los nombre de cada persona con las etiquetas de images como siguie:
    ```html
        <img src="/images/speakers/melissa-kerr.jpg" alt="Melissa Kerr"/>
        Melissa Kerr
    ```
    ```html
        <img src="/images/speakers/david-alexander.jpg" alt="David Alexander"/>
        David Alexander
    ```
    ```html
        <img src="/images/speakers/mark-hanson.jpg" alt="Mark Hanson"/>
        Mark Hanson
    ```
    ```html
        <img src="/images/speakers/april-meyer.jpg" alt="April Meyer"/>
        April Meyer
    ```
* En las páginas index y about sustituir los nombre de cada sponsor con las etiquetas de images como siguie:
    ```html
        <img src="/images/sponsors/sponsor1.png" alt="Trey Research"/>
    ```
    ```html
        <img src="/images/sponsors/sponsor2.png" alt="Litware, Inc"/>
    ```
    ```html
        <img src="/images/sponsors/sponsor3.png" alt="Fourth Coffee"/>
    ```
    ```html
        <img src="/images/sponsors/sponsor4.png" alt=" Graphic Design Institute "/>
    ```
    ```html
        <img src="/images/sponsors/sponsor5.png" alt=" Southridge Video "/>
    ```

#### Paso 4: Agregar la página About

* Agregar en el proyecto una nueva página html: **about**
* Agregar en la etiqueta **&lt;title&gt;**:
    ```html
        About ContosoConf
    ```
* Agregar dentro de la etiqueta **&lt;body&gt;** la siguiente etiqueda header. Esto es copiado de la página index:
    ```html
        <header>
            <h1>ContosoConf</h1>
            <p>A two-track conference on the latest HTML5 developments</p>
        </header>
    ```
* Despues de la etiqueta **&lt;/header&gt;** en la página about agregar:
    ```html
        <article>
            <h1>ContosoConf brings web designers and developers together</h1>
            <section>
                <p>
                    Since the very first Contoso Conf back in 2009, we've been guided by three principles:
                </p>
                <ol>
                    <li>Community Matters</li>
                    <li>Never Stop Learning</li>
                    <li>Have fun!</li>
                </ol>
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed vitae enim arcu, vitae aliquet purus. 
                    Aenean rhoncus diam et orci porttitor fringilla. In porta lacus a turpis pretium placerat. Cras viverra 
                    enim eu nibh pretium ornare. Praesent et adipiscing turpis. Duis mi risus, ornare at bibendum a, 
                    ullamcorper vel tellus. Nulla in egestas velit. Aenean consequat mi sed tellus iaculis laoreet. Donec et odio vel felis commodo porttitor.
                </p>
                <p>
                    Aenean id ligula est. Pellentesque ut magna ligula. Donec nunc eros, tincidunt sit amet sollicitudin 
                    in, semper id mauris. Phasellus odio nulla, molestie ac gravida sed, dignissim in nisl. Nunc luctus 
                    lobortis massa at dapibus. Aenean turpis nibh, hendrerit nec congue et, elementum a justo. Aenean sit 
                    amet nulla odio. Cras feugiat porta risus nec pretium.
                </p>

                <h2>What's It All About?</h2>
                <p>
                    Donec vel sem ut dui vulputate porta. Phasellus imperdiet sapien a arcu adipiscing vitae adipiscing 
                    elit pharetra. Donec sed ante ut eros mattis bibendum non in erat. Donec sagittis, massa eu accumsan 
                    eleifend, eros justo cursus justo, id consequat mauris diam id magna. Vivamus quis tortor massa. Nam ipsum metus, dapibus ac facilisis sit amet, ullamcorper quis risus. Integer aliquet eleifend accumsan.
                </p>
                <blockquote>I had a fantastic time and learnt so much!</blockquote>
                <p>
                    Pellentesque facilisis blandit augue id rhoncus. Sed facilisis varius lectus, eget commodo purus dapibus 
                    nec. In hac habitasse platea dictumst. Etiam imperdiet facilisis malesuada. Nunc semper venenatis elit ac lobortis. Duis lorem lorem, pharetra ut scelerisque nec, consequat sed risus. Morbi rutrum nisl ut ipsum consectetur porttitor. Phasellus sed nunc id diam tempus congue in a leo.
                </p>
                <p>
                    Proin feugiat, turpis id tempor tempor, lorem libero malesuada.
                </p>
            </section>
        </article>
    ```
* Agregar en la etiqueta **&lt;body&gt;** antes de cerrar esta etiqueta en la página **index.htm**:
    ```html
        <footer>
            <p>
                Hosted by Contoso
            </p>
            <address>
                Conference Center<br />
                3 Somewhere Street<br />
                Seattle<br />
                WA 98343
            </address>
            <p>
                &#169; 2012 Contoso
            </p>
        </footer>
    ```

#### Pasos 5: Agregar vínculos de navegación

* Agregar en la página **index.htm** despues de **&lt;header&gt;** el siguiente código html:
    ```html
        <nav>
            <a href="/index.htm">Home</a>
            <a href="/about.htm">About</a>
        </nav>
    ```
* Repetir el paso anterior par la página **about.htm**. 

#### Paso 6: Ejecutar la aplicación web

* Asignar **index.htm**, como página de inicio
* En el menu **Debug**, clic **Start Debugging**.
* Verficar que las páginas construidas se muestran
*  Verficar que los vínculos de las páginas construidas se funcionan debidamente.


### Ejercicio 2: Usando estilos para las páginas creadas

#### Paso 1: Crear una nueva hoja de estilos 

* Crear en el proyecto una carpeta: **styles**.
* Agregar en la carpeta **styles** una hoja de estilos: **Style Sheet**, llamada; **site.css**.
* En la página **index.htm** después de la etiqueta **&lt;/head&gt;**, insertamos el siguiente código markup:
    ```html
        <link href="/styles/site.css" rel="stylesheet" type="text/css" />
    ```
* Hacemos lo mismo para la página **about.htm**.
* Agregamos antes de **&lt;/head&gt;**, el siguiente código markup:
    ```html
        <link href="/styles/site.css" rel="stylesheet" type="text/css" />
    ```

#### Paso 2: Agregar reglas CSS para el estilo de la páginas

* Abrir el archivo **site.css** y borrar todo su contenido.
* Agregar el siguiente CSS código::
    ```css
        html {
            /* font-size 62.5% makes 1rem equal 10px for easy size calculations. */
            font-size: 62.5%;
            font-family: Calibri, Arial, sans-serif;
            background-color: #EAEEFA;
        }

        body {
            margin: 0;
            /* Default font-size to about 18px */
            font-size: 1.8rem;
        }

        .container {
            padding: 0 1rem;
            max-width: 94rem;
            /* Horizontally center containers */
            margin: 0 auto;
        }

        nav {
            background-color: #1d1d1d;
            line-height: 6rem;
            font-size: 1.7rem;
        }

        nav a {
            color: #fff;
            padding: 1rem;
        }

        h1 {
            font-size: 4rem;
            letter-spacing: -1px;
            margin: 1em 0 .25em 0;
        }
    ```
* doble-clic en **index.htm**.
* Reemplazar el contenido de **&lt;nav&gt;** con lo siguiente:
    ```html
        <div class="container">
            <a href="/index.htm">Home</a>
            <a href="/about.htm">About</a>
        </div>
    ```
* Después de la etiqueta **&lt;/nav&gt;** y ante la etiqueta **&lt;header&gt;**, insertar el siguiente código HTML markup:
    ```html
        <div class="container">
    ```
	Cerrar el elemento **&lt;div&gt;**, antes de **&lt;/body&gt;**:
    ```html
        </div>
    ```
* En la página **about.htm**, reemplazar el contenido de  **&lt;nav&gt;** con el contenido HTML markup:
    ```html
        <div class="container">
            <a href="/index.htm">Home</a>
            <a href="/about.htm">About</a>
        </div>
    ```
* Despues de **&lt;/nav&gt;** y antes de **&lt;header&gt;**, insertar el siguientes contenido HTML markup:
    ```html
        <div class="container">
    ```
* Cerrar **&lt;div&gt;**, y antes de **&lt;/body&gt;** insertar el siguientes contenido HTML markup:
    ```html
        </div>
    ```
La página Home con el estilo aplicado tendría que verse como:
![alt text](./ContosoConf/ContosoConf/images/20480B_2_Home.png "Images screenshot")

#### Paso 3: Ejecutar la aplicación web 

1.	En el menu **Debug** menu, clic **Start Without Debugging**.
2.	Verificar que la  página **About** tiene el estilo propio de la página.
3.	Ir a la página **Home**, vefificar que esta página es consistente con la página **About**.
4.	Cerrar todo.
