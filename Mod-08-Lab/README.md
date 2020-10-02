## Modulo 8 - Creando página interactivas usando APIs de HTML5

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** 30 de Septiembre 2020.
3. **Resumen del Ejercicio:**
    * En este laboratorio hace uso Chrome DevTools que son un conjunto de herramientas de creación web y depuración integrado en Google Chrome. Usamos DevTools para iterar y depurar tu sitio, y para crear un perfil de él. 
    Algunos de los paneles que contiene son:
    * Device Mode - para desarrollar experiencias web con una completa capacidad de respuestas y que prioricen los dispositivos móviles. Emula sensores: ubicación geográfica y acelerómetro.
    * Elements - el panel de Elements se usa para iterar la distribución y el diseño de tu sitio mediante la libre manipulación de DOM y CSS. Además; Inspecciona y modifica ligeramente tus páginas, Edita estilos y Edita el DOM.
    * Console - para registrar información de diagnóstico durante el desarrollo o úsalo como un shell para interactuar con el código JavaScript en la página. Entro lo cual; Interactúa desde la línea de comandos.
    * Sources - Panel Sources Depura tu código JavaScript con puntos de interrupción en el panel Sources o conecta los archivos locales mediante espacios de trabajo para usar el editor en tiempo real de DevTools. Además; Depura con puntos de interrupción, Depura código ofuscado, Configura la persistencia con los espacios de trabajo de DevTools.
    * Network - el panel Network para obtener información sobre recursos solicitados y descargados, y optimizar el rendimiento de carga de tu página. Como por ejemplo; Conceptos básicos del panel Network, Comprensión de Resource Timing, Limitación de la red.
    * Timeline - el panel Timeline para mejorar el rendimiento del tiempo de ejecución de la página mediante la grabación y la exploración de los diferentes eventos que ocurren durante el ciclo de vida de un sitio. Además nos ayuda con; Cómo ver el rendimiento, Analizar el rendimiento del tiempo de ejecución,
    Diagnosticar diseños sincrónicos forzados.
    * Profiles - el panel Profiles si necesitas más información que la que proporciona el panel Timeline; por ejemplo, para rastrear pérdidas de memoria, también así se usa como; Generador de perfiles de CPU en JavaScript, Generador de perfiles de montón.
    * Application - el panel Resources para inspeccionar todos los recursos que se cargan; entre otros, bases de datos IndexedDB o Web SQL, almacenamiento local y de sesión, cookies, caché de la app, imágenes, fuentes y hojas de estilos, además de Administrar datos.
    
4. **Dificultad o problemas presentados y como se resolvieron:** La experiencia nueva de usar F12 es la única dificultad. Hay caracteristicas que no son las mismas en diferentes navegadores. En mi caso yo uso Chrome por eso enfoco el desarrollo de este laboratorio a Chrome. 

Fecha de entrega: Martes 29 de septiembre de 2020

>**Objetivos**: 
* En este laboratorio hace uso de Chrome DevTools que son un conjunto de herramientas de creación web y depuración integrado en Google Chrome. Usamos DevTools para iterar y depurar tu sitio, y para crear un perfil de él. En el resumen del ejercicio indicamos los diferentes paneles con los cuales nos vamos a familirizar en este laboratorio.

Dondequiera que la ruta de un archivo comience con *[Raíz del repositorio]*, reemplácela con la ruta absoluta de la carpeta en la que reside el repositorio 20480. Por ejemplo, si clonaste o extrajiste el repositorio 20480 a to**C:\Users\John Doe\Downloads\20480**, cambiar la ruta de:**[Repository Root]\AllFiles\20480C\Mod01** a**C:\Users\John Doe\Downloads\20480\AllFiles\20480C\Mod01**.


## Ejercicio 1: Arrastrar y soltar imágenes

### Tarea 1: Revisar el marcado HTML y el código JavaScript de la página de la insignia de orador

1.	Abrir Microsoft Visual Studio 2019.
2.	En Visual Studio, en el menú **Archivo**, apunta a **Abrir**, y luego selecciona **Proyecto/Solución**.
3.	En el cuadro de diálogo **Abrir Proyecto**, ve a **[Repository Root]\Allfiles\Mod08\Labfiles\Starter\Exercise 1**, clic en **ContosoConf.sln**, y luego haz clic en **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
4.	En **Solution Explorer**, expandir el nodo de proyecto **ContosoConf**. 
5.	En **Solution Explorer**, haga doble clic en **speaker-badge.htm**.
6.	Verifique que el marcado HTML contiene el siguiente elemento **&lt;img;**:

    ```html
        <img style="width: 300px; height: 300px; border: 1px solid #000"/>
    ```
7.	Verifique que el marcado HTML contiene el siguiente elemento **&lt;script&gt;**:
    ```html
        <script src="/scripts/pages/speaker-badge.js" type="module"></script>
    ```
8.	En **Solution Explorer**, expande la carpeta **scripts**, y luego expande la carpeta **pages**.
9.	Haz doble clic en **speaker-badge.js**.
10.	Verifique que el archivo JavaScript contiene la siguiente línea de código:

    ```javascript
        new SpeakerBadgePage(badgeElement);
    ```

### Tarea 2: Añadir un evento de arrastrar y soltar oyentes

1.	En **SpeakerBadgePage.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Add event listeners for element "dragover" and "drop" events.
        //       handle with this.handleDragOver.bind(this) and this.handleDrop.bind(this)
2.	Después del comentario, añade el siguiente código JavaScript    

    ```javascript
        element.addEventListener("dragover", this.handleDragOver.bind(this), false);
        element.addEventListener("drop", this.handleDrop.bind(this), false);
    ```
####Tarea 3: Manejar el evento de la caída

1.	En **SpeakerBadgePage.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Get the files from the event
    ```

2.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        const files = event.dataTransfer.files;
    ```
3.	Encuentra el siguiente comentario:
    ```javascript
        // TODO: Read the first file in the array
    ```
4.	Después del comentario, añade el siguiente código JavaScript:
    ```javascript
        const file = files[0];
    ```
5.	Encuentra el siguiente comentario
    ```javascript
        //       Check the file type is an image
    ```
6.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        if (this.isImageType(file.type)) {
    ```

7.	Encuentra el siguiente comentario:
    ```javascript
         //       Use this.readFile to read the file, then display the image
         //       (Note that this.readFile returns a Promise, so chain ((file)=> this.displayImage(file)) using the "then" method.)
    ```
8.	Después del comentario, agregue el siguiente código JavaScript:

    ```javascript
			this.readFile(file).then((file)=> this.displayImage(file));
        } else {
            alert("Please drop an image file.");
        }
    ```
### Tarea 4: Leer la imagen usando un objeto FileReader

1.	En **SpeakerBadgePage.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Create a new FileReader
    ```
2.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        const reader = new FileReader();
    ```
3. Encuentra el siguiente comentario:
    ```javascript
        // TODO: Assign a callback function for reader.onload

        // TODO: In the callback use resolve([fileDataUrl]); to return the file data URL.
    ```
4.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        reader.onload = function (loadEvent) {
            const fileDataUrl = loadEvent.target.result;
            resolve([fileDataUrl]);
        };
    ```
5. Encuentra el siguiente comentario:
    ```javascript
        // TODO: Start reading the file as a DataURL
    ```
6.	Después del comentario, agregue el siguiente código JavaScript:

    ```javascript
        reader.readAsDataURL(file);
    ```

### Tarea 5: Probar la página de la insignia de orador

1.	En **Solution Explorer**, haga doble clic en **speaker-badge.htm**.
2.	En el menú **Debug**, haga clic en **Iniciar sin depuración**.
3.	En Microsoft Edge, si aparece el mensaje **Configuración de la Intranet desactivada por defecto**, haga clic en **No mostrar este mensaje de nuevo**.
4.	En la barra de tareas de Windows, haz clic en **Explorador de Archivos**, y luego busca **[Repository Root]\Allfiles\Mod08\Labfiles\Resources**.
5.	Arrastra y suelta **mark-hanson.jpg** desde el Explorador de Archivos, en el rectángulo vacío de Microsoft Edge.

![alt text](./Images/20480B_8_speaker-badge-01.png "The Speaker Badge page with the speaker's photo")

6.	Cierre el Explorador de archivos y el Explorador de bordes de Microsoft. 

>**Resultados**: Después de completar este ejercicio, habrá implementado la funcionalidad que permite al usuario arrastrar y soltar una imagen desde el Explorador de Archivos a la página web.

### Ejercicio 2: Incorporación de video

#### Tarea 1: Añadir un reproductor de vídeo a la página de inicio

1.	En Visual Studio, en el menú **Archivo**, apunta a **Abrir**, y luego selecciona **Proyecto/Solución**.
2.	En el cuadro de diálogo **Abrir Proyecto**, busca a
**[Repository Root]\Allfiles\Mod08\Labfiles\Starter\Exercise 2**, haga clic en **ContosoConf.sln**, y luego haga clic en **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
3.	En **Solution Explorer**, expande el nodo de proyecto **ContosoConf**.
4.	Haga doble clic en **index.htm**.
5.	Encuentra el comentario que comienza con la línea:
    ```javascript
        <!-- TODO: Add video tag here -->
    ```
6.	Después de la segunda línea del comentario, agregue el siguiente marcado HTML:
    ```html
        <video src="http://ak.channel9.msdn.com/ch9/265b/9a76fccd-941e-4285-ad00-9ea200aa265b/MIX09KEY01_high_ch9.mp4"></video>
    ```
### Tarea 2: Añadir controles al reproductor de vídeo

1.	En **index.htm**, después del elemento **&lt;/video&gt;**, inserte el siguiente marcado HTML:
    ```html
        <div class="video-controls" style="display: none">
            <button class="video-play">Play</button>
            <button class="video-pause">Pause</button>
            <span class="video-time"></span>
        </div>
    ```
2.	Busca el siguiente comentario y selecciónalo con el ratón:

    ```html
        <!--<script src="/scripts/pages/video.js" type="module"></script>-->
    ```
3.	En la barra de herramientas, haga clic en el botón **Descargar las líneas seleccionadas**. 
4.	Verifica que el marcado HTML ahora se ve así:
    ```html
        <script src="/scripts/pages/video.js" type="module"></script>
    ```
### Tarea 3: Controlar el video usando el código JavaScript

1.	En **Solution Explorer**, expande la carpeta **scripts**, y luego expande la carpeta **pages**.
2.	Haz doble clic en **video.js**.
3.	Encuentra el siguiente comentario:
    ```javascript
        // TODO: display the video controls
    ```
4.	Después de este comentario, añade el siguiente código JavaScript:

    ```javascript
        controls.style.display = "block";
    ```
5.	Encuentra el comentario que comienza con las siguientes líneas:
```javascript
        // TODO: Add event listeners for:
        //       video loaddata
```
6.	Después de la segunda línea de comentario, agregue el siguiente código JavaScript:
    ```javascript
        video.addEventListener("loadeddata", ready, false);
    ```
7.	En **video.js**, encuentra el siguiente comentario:

    ```javascript
        // TODO: play the video
    ```

8.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        video.play();
        playButton.style.display = "none";
        pauseButton.style.display = "";
    ```
9. Encuentra el siguiente comentario:
    ```javascript
        // TODO: pause the video
    ```
10.	Después del comentario, agregue el siguiente código JavaScript:

``` javascript
        video.pause();
        pauseButton.style.display = "none";
        playButton.style.display = "";
```

11. Encuentra el siguiente comentario:
    ```javascript
        //       play click
        //       pause click
    ```

12.	Después del comentario, agregue el siguiente código JavaScript:

    ```javascript
        playButton.addEventListener("click", play, false);
		pauseButton.addEventListener("click", pause, false);
    ```

### Tarea 4: Mostrar el vídeo del tiempo transcurrido

1.	En **video.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Set time.textContent using video.current time.
        //       Use the formatTime function to convert raw seconds into HH:MM:SS format.
    ```
2.	Después del comentario, agregue el siguiente código JavaScript:

    ```javascript
        time.textContent = formatTime(video.currentTime);
    ```

3. Encuentra el siguiente comentario:

    ```javascript
        //       video timeupdate
    ```
4.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        video.addEventListener("timeupdate", updateTime, false);
    ```

### Tarea 5: Probar el reproductor de vídeo

1.	En **Solution Explorer**, haga doble clic en **index.htm**.
2.	En el menú **Debug**, haga clic en **Iniciar sin depuración**.
3.	En Microsoft Edge, espera a que el botón **Play** aparezca debajo del video.
4.	Haga clic en **Reproducir**.
5.	Verifique que el vídeo comience a reproducirse y que se muestre la hora actual del vídeo.
6.	Haga clic en **Pausa**.
7.	Verifica que el video se pausa.
8.	Cierra Microsoft Edge.


>**Resultados**: Después de completar este ejercicio, habrás añadido un reproductor de vídeo a la página de inicio.

## Ejercicio 3: Uso de la API de geolocalización para informar de la ubicación actual del usuario

### Tarea 1: Revisar el marcado HTML y el código JavaScript

1.	En Visual Studio, en el menú **Archivo**, apunta a **Abrir**, y luego selecciona **Proyecto/Solución**.
2.	En el cuadro de diálogo **Abrir Proyecto**, apunta a **[Repository Root]\Allfiles\Mod08\Labfiles\Starter\Exercise 3**, clic en **ContosoConf.sln**, y luego a **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
3.	En **Solution Explorer**, expande el nodo de proyecto **ContosoConf**.
4.	En **Solution Explorer**, haga doble clic en **location.htm**.
5.	Verifique que el marcado HTML contiene el siguiente elemento **&lt;h2
    ```html
        <h2 id="distance"></h2>
    ```
6.	En **Solution Explorer**, expande la carpeta **scripts**, y luego expande la carpeta **pages**.
7.	Haz doble clic en **location.js**.
8.	8. Verifique que el archivo contiene el siguiente código JavaScript:

    ```javascript
        const conferenceLocation = {
            latitude: 47.6097,  // decimal degrees
            longitude: -122.3331 // decimal degrees
        };
    ```

### Tarea 2: Obtener la ubicación actual del usuario que está viendo la página

1.	En **location.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Get current position from the geolocation API.
		//       Call updateUIForPosition for success and error for failure.
    ```
2.	Después del comentario, agregue el siguiente código JavaScript:
    ```javascript
        navigator.geolocation.getCurrentPosition(updateUIForPosition, error);
    ```


### Tarea 3: Mostrar la distancia al lugar de la conferencia

1.	En **location.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Calculate the distance from the conference
    ```
2.	Después del comentario, agregue el siguiente código JavaScript:

    ```javascript
        const distance = distanceFromConference(position.coords);
    ```


### Tarea 4: Probar la página de localización

1.	En **Solution Explorer**, haga doble clic en **location.htm**.
2.	En el menú **Debug**, haga doble clic en **Start Without Debugging**.
3.	En **Microsoft Edge, si aparece el mensaje "Let localhost use your location?**", haga clic en **Sí**.
4.	En el cuadro de diálogo **Dejar que Microsoft Edge acceda a tu ubicación precisa?**, haz clic en **Sí**.
5.	Verifique que la página muestre la distancia a la sede de la conferencia, en millas (el valor real variará, dependiendo de su distancia a la sede de la conferencia).
6. Cierre todas las ventanas abiertas.

>**Resultados**: Después de completar este ejercicio, tendrás una página de **Localización** que muestra la distancia del usuario del lugar de la conferencia.

