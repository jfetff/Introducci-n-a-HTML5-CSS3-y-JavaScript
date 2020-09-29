## Laboratorio Módulo 5 Comunicarse con un servidor remoto

Fichero de Instrucciones: Instructions\20480C_MOD05_LAK.md

Entregar el url de GitHub con la solución y un readme con las siguiente información:

1. **Nombres y apellidos:** Jose Rene Fuentes Cortez
2. **Fecha:** 29 de Septiembre 2020.
3. **Resumen del Ejercicio:** 
    1. En el ejercicio 1 se modifica la página **schedule** para mostrar la lista de sesiones almacenadas en el servicio Web y al mismo tiempo se manejan los errores que pueden ocurrir cuando se comunica con un sistema remoto.
    2. El ejercicio 2 actualiza la página **schedule** y envía solicitudes para atender sesiones por parte de los participantes como un servicio Web. Después de un número de sesiones escogidas se muestra un mensaje por medio de un **alert** de forma amigable.
    3. El ejercicio 4 nos muestra como refactorizar el código de javaScript que envía y recibe datos usando métodos de JQuery con ajaz.
4. **Dificultad o problemas presentados y como se resolvieron:** Al inicio parecía que los ejercicios no corrían y eso es porque el cache del navegador se mantenía y no se mostraban por ejemplos las "stars" en las sesiones que se quiere seleccionar. Una vez que limplia el cache del navegador el ejercicio se concluye como se debe.

**NOTA**: Si no hay descripcion de problemas o dificultades, y al yo descargar el código para realizar la comprobacion y el código no funcionar, el resultado de la califaciación del laboratorio será afectado.

Fecha de entrega: Viernes 25 de septiembre de 2020



# Laboratorio: Comunicación con una fuente de datos remota

### Configuración de laboratorio

### Pasos de preparación

Asegúrese de haber clonado el directorio 20480C de GitHub (**https: //github.com/MicrosoftLearning/20480-Programming-in-HTML5-with-JavaScript-and-CSS3/tree/master/Allfiles**). Contiene los segmentos de código para los laboratorios y demostraciones de este curso.

### Ejercicio 1: Recuperar datos

#### Tarea 1: Revisar la página de programación

1. Abra Microsoft Visual Studio 2019.
2. En Microsoft Visual Studio, en el menú **Archivo**, seleccione **Abrir** y luego seleccione **Proyecto/Solución**.
3. En el cuadro de diálogo **Abrir proyecto**, vaya a **[Repository Root]\Allfiles\Mod05\Labfiles\Starter\Exercise 1**, haga clic en **ContosoConf.sln** y luego haga clic en **Abrir**.
> ** Nota **: Si aparece el cuadro de diálogo ** Advertencia de seguridad para ContosoConf**, desactive la casilla de verificación **Preguntarme por todos los proyectos de esta solución** y luego haga clic en **Aceptar**.
4. En **Explorador de soluciones**, expanda el proyecto **ContosoConf**, expanda la carpeta **scripts** y luego expanda la carpeta **páginas**.
5. Haga doble clic en **schedule.js**.
6. Verifique que la primera línea del archivo ahora contenga el siguiente código JavaScript:
    ```javascript
        dejar horario = [];
    ```
7. Verifique que la función **createSessionElement** contenga el siguiente código JavaScript:
    ```javascript
        function createSessionElement (sesión) {
            const li = document.createElement ("li");

            li.sessionId = session.id;

            estrella constante = document.createElement ("a");
            star.setAttribute ("href", "#");
            star.setAttribute ("clase", "estrella");
            li.appendChild (estrella);

            título const = document.createElement ("intervalo");
            title.textContent = session.title;
            li.appendChild (título);

            return li;
        };
    ```

### Tarea 2: Crear la función downloadSchedule

1. En el archivo **schedule.js**, busque el comentario que comienza con el siguiente texto:
    ```javascript
        // TODO: Crea una función llamada downloadSchedule
    ```
2. Después de la última línea de este comentario, agregue el siguiente código JavaScript:
    ```javascript
        function downloadSchedule () {
            solicitud constante = nueva XMLHttpRequest ();
        }
    ```
3. En el archivo **schedule.js**, después de la declaración anterior en la función **downloadSchedule**, agregue el siguiente código JavaScript:
    ```javascript
        request.open("GET", "/schedule/list", true);
        request.onreadystatechange = function () {
            if (request.readyState === 4) {
                const response = JSON.parse(request.responseText);
                response.schedule.forEach(function (element) {
                    schedule.push(element);
                });
                displaySchedule();
            }
        };
        request.send();
    ```
4. Agregue la siguiente declaración al final del archivo **schedule.js**:
    ```javascript
        downloadSchedule ();
    ```

#### Tarea 3: Agregar manejo de errores a la función downloadSchedule

En el archivo ** schedule.js **, agregue el siguiente código que se muestra en negrita a la función ** downloadSchedule **:
```javascript
        function downloadSchedule() {
            const request = new XMLHttpRequest();
            request.open("GET", "/schedule/list", true);
            request.onreadystatechange = function () {
                if (request.readyState === 4) {
                    try {
                        const response = JSON.parse(request.responseText);
                        if (request.status === 200) {
                            response.schedule.forEach(function (element) {
								schedule.push(element);
							});
                            displaySchedule();
                        } else {
                            alert(response.message);
                        }
                    } catch (exception) {
                        alert("Schedule list not available.");
                    }
                }
            };
            request.send();
        }
```

### Tarea 4: Probar la página Programación

1. En **Explorador de soluciones**, haga doble clic en **schedule.htm**.
2. En el menú **Depurar**, haga clic en **Iniciar sin depurar**.
3. En el navegador, si aparece el mensaje **La configuración de la intranet está desactivada de forma predeterminada**, haga clic en ** No volver a mostrar este mensaje**.
4. Verifique que la página muestre una lista de sesiones de conferencia.
5. Cierre Navegador.
6. En ContosoConf - Microsoft Visual Studio, haga doble clic en el archivo **schedule.js**.
7. En la función **downloadSchedule**, busque la siguiente declaración:
    ```javascript
       request.open("GET", "/schedule/list", true);
    ```
8. Cambie la URL en esta declaración como se muestra en el siguiente código:
    ```javascript
        request.open("GET", "/schedule/list?fail", true);
    ```
9. En el menú **Depurar**, haga clic en **Iniciar sin depurar**.
10. En el navegador, en la barra de navegación, haga clic en **Programar**.
11. Verifique que aparezca el mensaje **Servicio actualmente no disponible**.
12. En el cuadro de diálogo ** Mensaje de la página web **, haga clic en **Aceptar**.
13. Cierre el navegador.
14. En ContosoConf - Microsoft Visual Studio, en **Explorador de soluciones**, haga doble clic en el archivo **schedule.js**.
15. En la función * downloadSchedule**, cambie la cadena **/ schedule/list?Fail** de nuevo a **/schedule/list**.
16. En el menú **Archivo**, haga clic en **Guardar todo**.

> **Resultados**: Después de completar este ejercicio, habrá modificado el código de la página **Programación** para mostrar la lista de sesiones recuperadas de un servicio web y para manejar errores que pueden ocurrir al comunicarse con un control remoto. Servicio.

### Ejercicio 2: serializar y transmitir datos

#### Tarea 1: envía la solicitud para indicar la sesión que un asistente ha seleccionado

1. En ContosoConf - Microsoft Visual Studio, en el menú **Archivo**, seleccione **Abrir** y luego seleccione **Proyecto/Solución**.
2. En el cuadro de diálogo **Abrir proyecto**, vaya a **Repository Root]\Allfiles\Mod05\Labfiles\Starter\Exercise 2**, haga clic en **ContosoConf.sln** y, a continuación, haga clic en **abrir**.
> **Nota**: Si aparece el cuadro de diálogo **Advertencia de seguridad para ContosoConf**, desactive la casilla de verificación **Preguntarme por todos los proyectos de esta solución** y luego haga clic en **Aceptar**.
3. En **Explorador de soluciones**, expanda el proyecto **ContosoConf**, expanda la carpeta **scripts** y luego expanda la carpeta **páginas**.
4. Haga doble clic en **schedule.js**.
5. Busque la siguiente función:
    ```javascript
        función saveStar (sessionId, isStarred) {
    ```
6. Después de la última línea del comentario **TODO** en el cuerpo de esta función, agregue el siguiente código JavaScript:
    ```javascript
        solicitud constante = nueva XMLHttpRequest ();
        request.open ("POST", "/schedule/star/" + sessionId, verdadero);
    ```
7. Al final de la función **saveStar**, agregue el siguiente código JavaScript:
    ```javascript
    request.setRequestHeader ("Content-Type", "application/x-www-form-urlencoded");
    const data = "starred =" + isStarred;
    request.send (datos);
    ```

#### Tarea 2: Manejar la respuesta del servicio web

1. En el archivo **schedule.js**, busque la siguiente línea de código en la función ** **:
    ```javascript
         request.open ("POST", "/schedule/star/" + sessionId, verdadero);
    ```
2. Después de esta declaración, agregue el siguiente código JavaScript:
    ```javascript
        if (isStarred) {
            request.onreadystatechange = function() {
                if (request.readyState === 4 && request.status === 200) {
                    const response = JSON.parse(request.responseText);
                    if (response.starCount > 50) {
                        alert("This session is very popular! Be sure to arrive early to get a       seat.");
                    }
                }
            };
        }
    ```

#### Tarea 3: Probar la página Programación

1. En ** Explorador de soluciones **, haga doble clic en ** schedule.htm **.
2. En el menú ** Depurar **, haga clic en ** Iniciar sin depurar **.
3. En el navegador, haga clic en la estrella junto a ** Nuevas tecnologías en la empresa **.
4. Verifique que se muestre el siguiente mensaje de alerta:
    `` `javascript
        ¡Esta sesión es muy popular! Asegúrese de llegar temprano para conseguir un asiento.
    ''
5. En el cuadro de diálogo ** Mensaje de la página web **, haga clic en ** Aceptar **.
6. Haga clic en la estrella junto a ** Sumérjase en lo más profundo con Canvas **.
7. Verifique que no se muestre ningún mensaje de alerta.
8. Cierre el navegador.

> ** Resultados **: Después de completar este ejercicio, habrá actualizado la página ** Programación ** para enviar selecciones de asistentes a un servicio web y mostrar un mensaje cuando una sesión sea popular.


### Ejercicio 3: Refactorización del código mediante el método async await fetch.

#### Tarea 1: Refactorizar la función downloadSchedule

1. En ContosoConf - Microsoft Visual Studio, en el menú **Archivo**, seleccione **Abrir** y luego seleccione **Proyecto / Solución**.
2. En el cuadro de diálogo **Abrir proyecto**, vaya a **[Repository Root]\Allfiles\Mod05\Labfiles\Starter\Exercise 3**, haga clic en **ContosoConf.sln** y luego haga clic en **Abrir**.
> **Nota**: Si aparece el cuadro de diálogo **Advertencia de seguridad para ContosoConf**, desactive la casilla de verificación **Preguntarme por todos los proyectos de esta solución** y luego haga clic en **Aceptar**.
3. En el Explorador de soluciones, expanda la carpeta **scripts**, expanda la carpeta **páginas** y luego haga doble clic en **schedule.js**.
4. En el archivo **schedule.js**, reemplace la función **downloadSchedule** con el siguiente código JavaScript:
```javascript
		const downloadSchedule = async () => {
			   // await response of fetch call
			   let response = await fetch("/schedule/list");

			   // checking response is ok
			   if (response.ok) {
				   // transform body to json
				   let data = await response.json();
				   schedules = data.schedule;
				   displaySchedule();
			   }
			   else
				   alert("Schedule list not available.");
		}
```
#### Tarea 2: Refactorizar la función saveStar

En el archivo **schedule.js**, reemplace la función **saveStar** con el siguiente código JavaScript:
```javascript
	const saveStar = async (sessionId, isStarred) => {

		const headers = new Headers({
			"Content-Type": "application/x-www-form-urlencoded"
		})


		const options = {
			method: 'POST',
			headers: headers,
			body: "starred=" + isStarred
		}

		const response = await fetch("/schedule/star/" + sessionId, options);

		if (isStarred) {
			if (response.ok) {
				const data = await response.json();
				if (data.starCount > 50)
					alert("This session is very popular! Be sure to arrive early to get a seat.");
			}
		}
	}
```
#### Tarea 3: Probar la página Programación

1. En **Explorador de soluciones**, haga doble clic en **schedule.htm**.
2. En el menú **Depurar**, haga clic en **Iniciar sin depurar**.
3. En el navegador, verifique que la página muestre la lista de sesiones de conferencia.
4. Haga clic en el icono de estrella junto a **Nuevas tecnologías en la empresa**.
5. Verifique que se muestre el siguiente mensaje de alerta:
    ```javascript
        ¡Esta sesión es muy popular! Asegúrese de llegar temprano para conseguir un asiento.
    ```
6. En el cuadro de diálogo **Mensaje de la página web**, haga clic en **Aceptar**.
7. Haga clic en el icono de la estrella junto a **Buceando en el fondo con Canvas**.
8. Verifique que no se muestre ningún mensaje de alerta.
9. Cierre el navegador.
10. En Visual Studio, en **Explorador de soluciones**, haga doble clic en **schedule.js**.
11. En la función **downloadSchedule**, busque la cadena **/ schedule/list** y reemplácela con **/schedule/list?Fail**.
12. En **Explorador de soluciones**, haga doble clic en **schedule.htm**.
13. En el menú **Depurar**, haga clic en **Iniciar sin depurar**.
14. Verifique que se muestre el mensaje de error **Lista de programación no disponible**.
15. En el cuadro de diálogo **Mensaje de la página web**, haga clic en **Aceptar**.
16. Cierre el navegador.

> **Resultados**: Después de completar este ejercicio, habrá refactorizado el código JavaScript que envía y recibe datos para usar el método jQuery **ajax**.