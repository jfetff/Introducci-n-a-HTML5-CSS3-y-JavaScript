# Module 3 - Lab: Introducción a Javascript

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** 24 de Septiembre 2020.
3. **Resumen del Ejercicio:**
    * Agregar en la página **Schedule** para mostrar las sesiones de la conferencias de la aplicación **ContosoConf**.
    * Actualizar la página **Schedule** para filtrar las sesiones basada en que canal o trayectoria han sido seleccionadas.
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

#### Pasos 2: Escribir el código para obtener el elemento html para la lista de sesiones en la página Schedule

1.	En el Solution Explorer, doble-clic **schedule.js**.
2.	Después de la linea que contiene **TODO: Task 2**, escribir el siguiente código JavaScript:
    ```javascript
        const list = document.getElementById("schedule");
    ```

#### Pasos 3: Implementar la función createSessionElement function que crea un item de la lista para una sessión

1.	En **schedule.js**, después de la linea que contiene **TODO: Task 3**, escribir el siguiente código JavaScript:
    ```javascript
        const li = document.createElement("li");
        li.textContent = session.title;
        return li;
    ```

#### Pasos 4: Implementar la función displaySchedule que agrega un item de sesión a la lista para su visualización

1.	En **schedule.js**, después de la linea que contiene **TODO: Task 4**, escribir el siguiente código JavaScript:
    ```javascript
        for (let i = 0; i < schedule.length; i++) {
            const li = createSessionElement(schedule[i]);
            list.appendChild(li);
        }
    ```

#### Pasos 5: Run the web application and view the Schedule page

1.	En el Solution Explorer, doble-click **schedule.htm**.
2.	En el menu **Debug**, clic **Start Without Debugging**.
3.	Verificar que la lista de sesiones se visualizar.
4.	Cerrar todo.


>**Results**: After completing this exercise, you will have added the **Schedule** page, which displays the details of the conference sessions, to the ContosoConf application.



## Ejercicio 2: Manejando los eventos

#### Paso 1: Agregar etiquetas de casillas de verificación HTML

1.	En ContosoConf - Visual Studio >> **File** >> **Open** >> **Project/Solution**.
2.	Abrir **\Allfiles\Mod03\Labfiles\Start\Exercise 2** >> **ContosoConf.sln** >> **Open**.
3.	En el Solution Explorer, expandir el proyecto **ContosoConf**, doble-clic **schedule.htm**.
4.	Encontrar el contenido siguiente HTML markup:
    ```html
        <ul id="schedule"></ul>
    ```
5.	Antes de la linea anterior, escribir el siguientes código  HTML markup:
Show:
    ```html
        <input type="checkbox" id="show-track-1" checked="checked"/><label      for="show-track-1">Track 1</label>
        <input type="checkbox" id="show-track-2" checked="checked"/><label      for="show-track-2">Track 2</label>
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


## Ejercicio 2: Manejando Eventos

#### Paso 1: Agregar casillas de verificación HTML 

1.	En ContosoConf - Visual Studio >> **File** >> **Open** >> **Project/Solution**.
2.	En la casilla de dialogo **Open Project** >> **\Allfiles\Mod03\Labfiles\Start\Exercise 2** >> **ContosoConf.sln** >> **Open**.
3.	En el Solution Explorer, expandir el proyecto **ContosoConf**, y doble-clic **schedule.htm**.
4.	Encontrar el siguientes following HTML markup:
    ```html
        <ul id="schedule"></ul>
    ```
5.	Antes de esta última linea, inserte el siguiente HTML markup:
    ```html
        <input type="checkbox" id="show-track-1" checked="checked"/><label      for="show-track-1">Track 1</label>
        <input type="checkbox" id="show-track-2" checked="checked"/><label      for="show-track-2">Track 2</label>
    ```

#### Paso 2: Escribir el código para obtener las casillas de verificación de la página Schedule

1.	En Solution Explorer, expandir el folder **scripts**, expandir el subfolder **pages**, doble-clic **schedule.js**.
2.	En **schedule.js**, encontrar la linea de código que contiene el siguiente JavaScript:
    ```javascript
        const list = document.getElementById("schedule");
    ```
3.	Después de esta lina, agregar el siguientes código JavaScript:
    ```javascript
        const track1CheckBox = document.getElementById("show-track-1");
        const track2CheckBox = document.getElementById("show-track-2");
    ```

#### Paso 3: Agregar los eventos click listeners para cada casilla de verificación

1.	En **schedule.js**, agregar el siguientes código JavaScript al final del archivo:
    ```javascript
        track1CheckBox.addEventListener("click", displaySchedule, false);
        track2CheckBox.addEventListener("click", displaySchedule, false);
    ```

#### Paso 4: Actualizar la función displaySchedule para visualizar las sesiones de los ramas seleecionadas

1.	En el archivo **schedule.js**, en la función **displaySchedule**, reemplazar el cuerpo de bucle **for** con el siguiente código JavaScript:
    ```javascript
        const tracks = schedule[i].tracks;
        const isCurrentTrack = (track1CheckBox.checked && tracks.indexOf(1) >= 0) ||
                                (track2CheckBox.checked && tracks.indexOf(2) >= 0);
        if (isCurrentTrack) {
            const li = createSessionElement(schedule[i]);
            list.appendChild(li);
        }
    ```

#### Paso 5: Ejecutar la aplicación web y ver si la página Schedule actúa como debe

1.	En el Solution Explorer, doble-clic **schedule.htm**.
2.	En el menu **Debug**, clic **Start Without Debugging**.
3.	En el navegador, verificar que ambas casillas de verificación seleccionadas muestran la lista completa de las sesiones a visualizar.
4.	Limpiar **Track 1** y verificar que solo se muestras las sesiones para el **Track 2**.
5.	Seleccionar **Track 1**, limpiar **Track 2**, y verificar que solo se muestras las sesiones para el Track 1.
6.	Limpiar **Track 1** y verificar que ni se muestras ninguna de las sesiones.
7.	Cerrar el navegador.
6. Cerrar todo.
