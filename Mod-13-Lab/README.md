## Modulo 13: Aplicación de la comunicación en tiempo real mediante el uso de la web 

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** Jueves 1 de octubre de 2020.
3. **Resumen del Ejercicio:**
    * En este laboratorio haremos dos ejericios;
        * En el primer ejericio hacemos uso de técnicas para hacer una presentación amigable al usario. A la hora de imprimir por ejemplo se eliminan encabezado, pie de página entre otras cosas que no son necesarias y hacen la impresión más amigable.
        * En el segundo ejericicio usamos técnicas para mostrar solo la información que para el usuario es relevante por ejemplo en el factor de forma reducido (envolvente) y que al mostrar la barra de navegación el enlace **Registrarse** no aparezca en el encabezado de la página web. Además hacemos que la aplicación se adapte a las pantallas de los dispositivos.

    
4. **Dificultad o problemas presentados y como se resolvieron:** Ninguna presentada.

Fecha de entrega: Jueves 1 de octubre de 2020.

>**Objetivos**: 
* En este laboratorio tenemos como objetivo usar técnicas y herramientas que hacen la impresión al usuario más amigable. Queremos hacer la aplicación amigable para el usuario y para que cuando usa diferente dispositivos con diferentes tamaño de la pantalla del disposito solo se muestre las información relevante. También es aprender como hacer posible que la aplicación se adapte a la pantalla del móvil del usuario.

# Laboratorio: Realizar la comunicación en tiempo real mediante el uso de enchufes de la web

## Lab Setup

## Preparation Steps

Asegúrate de que has clonado el directorio 20480C de GitHub (**https://github.com/MicrosoftLearning/20480-Programming-in-HTML5-with-JavaScript-and-CSS3/tree/master/Allfiles**). Contiene los segmentos de código para los laboratorios y demostraciones de este curso.


## Ejercicio 1: Recibir mensajes de un enchufe de la red

### Tarea 1: Revisar la página en vivo

1.	Abrir **Microsoft Visual Studio 2017**.
2.	En Microsoft Visual Studio, en el menú **Archivo**, apunta a **Abrir**, y luego haz clic en **Proyecto/Solución**.
3.	En el cuadro de diálogo **Abrir Proyecto**, apunta a **[Repository Root]\Allfiles\Mod13\Labfiles\Starter\Exercise 1**, haz clic en **ContosoConf.sln**, y luego en **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
4.	En el menú **Debug**, haga clic en **Iniciar sin depuración**.
5.	En el navegador, si aparece el mensaje **Configuración de la Intranet desactivada por defecto**, haga clic en **No mostrar este mensaje de nuevo**.
6.	Haga clic en **Vivir**.
7.	Si aparece el cuadro de diálogo **Error de página web**, haga clic en **No**.
8.	Verifica que la página **En vivo** se vea como la siguiente imagen:

![alt text](./Imágenes/20480B_13_Live.png "La página en vivo")

9.	Cerrar el navegador y volver a **ContosoConf - Microsoft Visual Studio**.
10.	En **Solution Explorer**, expandir el proyecto **ContosoConf**, y luego hacer doble clic en **live.htm**.
11.	Verifique que esta página contiene el siguiente marcado HTML:
    ```html
        <form action="#">
            <label for="ask-question-text">Ask a question</label>
            <input id="ask-question-text" type="text" />
            <button type="submit">Ask</button>
        </form>
        <ul>
            <!-- Questions will be displayed here when received by the web socket. -->
        </ul>
    ```
12.	Verifique que la página contiene el siguiente marcado HTML:
     ```HTML
        <script src="/scripts/pages/live.js" type="module"></script>
    ```
13.	En **Solution Explorer**, expande la carpeta **scripts**, expande la carpeta **pages**, y luego haz doble clic en **live.js**.
14.	Verifica que el archivo contiene el siguiente código JavaScript:
    ```javascript
        nuevo LivePage(

    ```

#### Tarea 2: Recibir mensajes utilizando un enchufe de la web

1.	En **live.js**, encuentra el siguiente comentario cerca del principio del archivo:
    ```javascript
        // TODO: Create a web socket connection to ws://localhost:[port]/live/socket.ashx
    ```
2.	Después de este comentario, agregue el siguiente código JavaScript y cambie el **[port]** según el puerto de su aplicación:
    ```javascript
        const socket = new WebSocket("ws://localhost:[port]/live/socket.ashx");
    ```
3.	En el Explorador de Soluciones, expande la carpeta **scripts**, y luego haz doble clic en **LivePage.js**.
4.	Encuentra el siguiente comentario: 

    ```javascript
        // TODO: Assign a callback to handle messages from the socket.
    ```
5.	Después de este comentario, añade el siguiente código JavaScript:
    ```javascript
        this.socket.onmessage = this.handleSocketMessage.bind(this);
    ```

#### Tarea 3: Mostrar las preguntas recibidas como mensajes

1.	En **LivePage.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Parse the event data into message object.
    ```
2.	Después de este comentario, añade el siguiente código JavaScript:
    ```javascript
        const message = JSON.parse(event.data);
    ```
3.	Encuentra el siguiente comentario:
    ```javascript
        // TODO: Check if message has a `questions` property, before calling handleQuestionsMessage
    ```
4.	Modifique la declaración que sigue a este comentario, como se muestra a continuación:
    ```javascript
        if (message.questions) {
            this.handleQuestionsMessage(message);
        }
    ```
5.	Encuentra el siguiente código:
    ```javascript
        displayQuestion(question) {
            const item = this.createQuestionItem(question);
            //item.appendChild(this.createReportLink());
            this.questionListElement.appendChild(item);
        }
    ```
6.	Encuentra el siguiente comentario en la función **handleQuestionsMessage()**:
    ```javascript
        // TODO: Display each question in the page, using the displayQuestion function.
    ```
7.	Después de este comentario, añade el siguiente código JavaScript:
    ```javascript
       message.questions.forEach(this.displayQuestion, this);
    ```

#### Tarea 4: Probar la aplicación

1.	En el Explorador de soluciones, haga doble clic en **live.htm**.
2.	2. En el menú **Debug**, haga clic en **Start Without Debugging**.
3.	En el navegador, una vez que la página se haya cargado, espera cinco segundos.
4.	Verifique que la página muestra las siguientes cuatro preguntas:
- **¿Cuáles son algunos buenos recursos para empezar con HTML5?**
- **¿Puedes explicar más sobre el Web Socket API, por favor?**
- **¡Este es un mensaje inapropiado!**
- **¿Cuánto de CSS3 puedo usar ahora mismo?**
5.	Cerrar el navegador.

>**Resultados:** Después de completar este ejercicio, habrás añadido un código JavaScript a la página web **Live** para recibir preguntas de un web socket y para mostrarlas.

### Ejercicio 2: Enviando mensajes a un Web Socket

#### Tarea 1: Formatear una pregunta como un mensaje

1.	En ContosoConf - Microsoft Visual Studio, en el menú **Archivo**, apunte a **Abrir**, y luego haga clic en **Proyecto/Solución**.
2.	En el cuadro de diálogo **Abrir Proyecto**, apunta a **[Repository Root]\Allfiles\Mod13\Labfiles\Starter\Exercise 2**, apunta a **ContosoConf.sln**, y luego haz clic en **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
3.	En el Explorador de soluciones, expanda el proyecto **ContosoConf**, expanda la carpeta **scripts** y luego haga doble clic en **LivePage.js**.
4.	Verifique que el archivo **LivePage.js** contiene la siguiente función:

    ```javascript
        askQuestion(text) {
            // TODO: Create a message object with the format { ask: text }

            // TODO: Convert the message object into a JSON string

            // TODO: Send the message to the socket

            // Clear the input ready for another question.
            this.questionInput.value = "";
        }
    ```
5.	En la función **askQuestion()**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Create a message object with the format { ask: text }
    ```
6.	Después de este comentario, añade el siguiente código JavaScript:
    ```javascript
        const message = {
            ask: text
        };
    ```
7.	Encuentra el siguiente comentario:
    ```javascript
        // TODO: Convert the message object into a JSON string
    ```
8.	Después de este comentario, añade el siguiente código JavaScript:
    ```javascript
        const json = JSON.stringify(message);
    ```


### Tarea 2: Envía el mensaje al enchufe de la web

1.	En **LivePage.js**, encuentra el siguiente comentario:
    ```javascript    
        // TODO: Send the message to the socket
    ```
2.	Después de este comentario, añade el siguiente código JavaScript:
    ```javascript
        this.socket.send(json);
    ```

### Tarea 3: Probar la aplicación

1.	En el Explorador de soluciones, haga doble clic en **live.htm**.
2.	En el menú **Debug**, haga clic en **Start Without Debugging**.
3.	En el navegador, presione Ctrl + T para abrir una nueva pestaña.
4.	En la **Barra de direcciones**, escriba **http://localhost:[port]/live.htm**, y luego presione **ENTER**.
     >Nota: Cambie el [puerto] según el puerto de su aplicación.
5.	En la casilla **Pregunta**, escriba **Esto es una prueba.**, y luego pulse **Preguntar**.
6.	Verifique que la lista de preguntas muestra **Esto es una prueba.**
7.	Haga clic en la primera pestaña de el navegador.
8.	Verifique que la lista de preguntas incluye **Esto es una prueba.**
9.	Cierre el navegador.

>**Resultados:** Después de completar este ejercicio, habrás modificado la página de preguntas **En vivo** para permitir a los usuarios hacer preguntas enviando mensajes al servidor mediante el socket web.

## Ejercicio 3: Manejando diferentes tipos de mensajes de Web Socket.


### Tarea 1: Mostrar los enlaces del informe

1.	En ContosoConf - Microsoft Visual Studio, en el menú **Archivo**, apunte a **Abrir**, y luego haga clic en **Proyecto/Solución**.
2.	2. En el cuadro de diálogo **Abrir Proyecto**, apunta a **[Repository Root]\Allfiles\Mod13\Labfiles\Starter\Exercise 3**, apunta a **ContosoConf.sln**, y luego haz clic en **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
3.	En el Explorador de soluciones, expanda el proyecto **ContosoConf**, expanda la carpeta **scripts** y luego haga doble clic en **LivePage.js**.
4.	4. En **LivePage.js**, encuentra el siguiente código:

    ```javascript
        createReportLink() {
            const report = document.createElement("a");
            report.textContent = "Report";
            report.setAttribute("href", "#");
            report.setAttribute("class", "report");
            return report;
        }
    ```
5.	En la función **displayQuestion()**, encuentra el siguiente comentario:
    ```javascript
        //item.appendChild(this.createReportLink());
    ```
6.	Modifique esta declaración y elimine los caracteres __//__, como se muestra en el siguiente código JavaScript:
    ```javascript
        item.appendChild(this.createReportLink());
    ```

#### Tarea 2: Enviar el mensaje del informe

1.	En **LivePage.js**, encuentra la siguiente función:
    ```javascript
        handleQuestionsClick(event) {
            event.preventDefault();

            const clickedElement = event.srcElement || event.target;
            if (this.isReportLink(clickedElement)) {
                const questionId = clickedElement.parentNode.questionId;
                this.reportQuestion(questionId);
                clickedElement.textContent = "Reported";
            }
        }
    ```
2.	En la función **reportQuestion()**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Send socket message { report: questionId }
    ```
3.	Después del comentario, añade el siguiente código:
    ```javascript
        this.socket.send(JSON.stringify({ report: questionId }));
    ```

#### Tarea 3: Manejar los mensajes de las preguntas

1.	En **LivePage.js**, encuentra la función **handleRemoveMessage()**:
    ```javascript
        handleRemoveMessage(message) {
            const listItems = this.questionListElement.querySelectorAll("li");
            for (let i = 0; i < listItems.length; i++) {
                if (listItems[i].questionId === message.remove) {
                    this.questionListElement.removeChild(listItems[i]);
                    break;
                }
            }
        }
    ```
2.	Encuentra el método **handleSocketMessage**:
    ```javascript
        handleSocketMessage(event) {
            // TODO: Parse the event data into message object.
            const message = JSON.parse(event.data);

            // TODO: Check if message has a `questions` property, before calling handleQuestionsMessage
            if (message.questions) {
                this.handleQuestionsMessage(message);
            }
        }
    ```
3.	Modificar el código JavaScript en el método **handleSocketMessage** como se muestra a continuación:
    ```javascript
        handleSocketMessage: function (event) {
            // TODO: Parse the event data into message object.
            const message = JSON.parse(event.data);
            if (message.questions) {
                this.handleQuestionsMessage(message);
            } else if (message.remove) {
                this.handleRemoveMessage(message);
            }
        }
    ```

#### Tarea 4: Probar la aplicación

1.	En el Explorador de soluciones, haga doble clic en **live.htm**.
2.	2. En el menú **Debug**, haga clic en **Start Without Debugging**.
3.	3. En el navegador, después de que se cargue la página, espere cinco segundos.
4.	Junto a **Cuáles son algunos buenos recursos para empezar con 


















