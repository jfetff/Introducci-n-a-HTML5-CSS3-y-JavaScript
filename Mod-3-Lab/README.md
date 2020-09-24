# Module 3 - Lab: Introducción a Javascript

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** 24 de Septiembre 2020.
3. **Resumen del Ejercicio:**
    * Agregar en la página **Schedule** para mostrar las sesiones de la conferencias de la aplicación **ContosoConf**.
    * El principal objetivo de este laboratorio es actualizar la página **Schedule** para filtrar las sesiones basada en que canal o trayectoria han sido seleccionadas.
4. **Dificultad o problemas presentados y como se resolvieron:** Ninguna dificultad.

Fecha de entrega: Jueves 24 de septiembre de 2020

>**Objetivos**: 
* Agregar en la página **Schedule** para mostrar las sesiones de la conferencias de la aplicación **ContosoConf**.
* El principal objetivo de este laboratorio es actualizar la página **Schedule** para filtrar las sesiones basada en que canal o trayectoria han sido seleccionadas.

## Lab Pasos

## Ejercicio 1: Visualizando Datos de manera programática

#### Paso 1: Revisar el código existente en la página Schedule

* Abrir Visual Studio 2019
* Crear un nuevo proyecto: **ContosoConf**.

1.	Abrir Microsoft Visual Studio 2019.
2.	Abrir el proyecto dado **\Allfiles\Mod03\Labfiles\Starter\Exercise 1**, clic **ContosoConf.sln**.
4.	Doble-clic en **schedule.htm**.
5.	Revisar el contenido de **schedule.htm** que contengas lo siguiente:
    ```html
        <section class="page-section schedule">
            <div class="container">
                <h1>Schedule</h1>
                <ul id="schedule"></ul>
            </div>
        </section>
    ```
6.	Verificar que contenga:
    ```html
        <script src="/scripts/pages/schedule.js" type="text/javascript"></script>
    ```
7.	En el Solution Explorer >> **scripts** >> **pages** >> doble-clic en **schedule.js**.
8.	Revisar el contenido de **schedule.js** que contenga:
    ```javascript
        const schedule = [ 
            {
                "id": "session-1",
                "title": "Registration",
                "tracks": [1, 2]
            },
            {
                "id": "session-2",
                "title": "Moving the Web forward with HTML5",
                "tracks": [1, 2]
            },
            {
                "id": "session-3",
                "title": "Diving in at the deep end with Canvas",
                "tracks": [1]
            },
            {
                "id": "session-4",
                "title": "New Technologies in Enterprise",
                "tracks": [2]
            },
            ...
        ];
    ```

#### Ejercicio 2: Manejando los eventos

#### Paso 1: Agregar etiquetas de casillas de verificación HTML

* Agregar un header en la pagina
* Agregar una etiqueta section
1.	En el Solution Explorer, doble-clic **schedule.js**.
2.	Después de la linea que contiene **TODO: Task 2**, agregar la siguiente linea de JavaScript:
    ```javascript
        const list = document.getElementById("schedule");
    ```

#### Paso 3: Implementar la función que crea un lista de items para una sesión

1.	En **schedule.js**, después de la lines que contiene **TODO: Task 3**, agregar el siguiente código JavaScript:
    ```javascript
        const li = document.createElement("li");
        li.textContent = session.title;
        return li;
   ```

#### Paso 4: Implementar la función  displaySchedule que agrega items a la lista para su visualización

1.	En **schedule.js**, después de la linea que contiene **TODO: Task 4**, agregar el siguiente código JavaScript:
    ```javascript
        for (let i = 0; i < schedule.length; i++) {
            const li = createSessionElement(schedule[i]);
            list.appendChild(li);
        }
    ```

#### Pasos 5: Ejecutar la aplicación web y ver la página schedule

1.	En el Solution Explorer, doble-clic **schedule.htm**.
2.	En el menu **Debug**, clic **Start Without Debugging**.
3.	Verificar que la lista de sesiones se visualiza.
4.	Cerrar el Navegador.


## Ejercicio 2: Usando estilos para las páginas creadas

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
