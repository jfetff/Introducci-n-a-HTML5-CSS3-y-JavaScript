# Módulo 7: Crear objetos y métodos usando JavaScript

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** 24 de Septiembre 2020.
3. **Resumen del Ejercicio:**
    * En este laboratorio hace uso de objetos para refactorizar el código JavaScript para que la página **Calendario** sea más mantenible. La idea es aprender a refactorizar el código JavaScript.
    
4. **Dificultad o problemas presentados y como se resolvieron:** Ninguna dificultad.

Fecha de entrega: Jueves 24 de septiembre de 2020

>**Objetivos**: 
* En este laboratorio hace uso de objetos para refactorizar el código JavaScript para que la página **Calendario** sea más mantenible. La idea es aprender a refactorizar el código JavaScript.

Dondequiera que la ruta de un archivo comience con *[Raíz del repositorio]*, reemplácela con la ruta absoluta de la carpeta en la que reside el repositorio 20480. Por ejemplo, si clonaste o extrajiste el repositorio 20480 a to **C:\Users\John Doe\Downloads\20480**, cambiar la ruta de: **[Repository Root]\AllFiles\20480C\Mod01** a **C:\Users\John Doe\Downloads\20480\AllFiles\20480C\Mod01**.

# Laboratorio: Refinando el código de mantenimiento y extensibilidad.

### Pasos de Preparación

Asegúrate de que has clonado el directorio 20480C de GitHub (**https://github.com/MicrosoftLearning/20480-Programming-in-HTML5-with-JavaScript-and-CSS3/tree/master/Allfiles**). Contiene los segmentos de código para los laboratorios y demostraciones de este curso.


## Ejercicio 1: Refactorización del código JavaScript para usar clases y objetos

#### Tarea 1: Crear la clase ScheduleList

1.	En Microsoft Visual Studio, en el menú **Archivo**, apunta a **Abrir**, y luego haz clic en **Proyecto/Solución**.
2.	En el cuadro de diálogo **Abrir Proyecto**, apunta a **[Raíz del Repositorio]\AllFiles\Mod07\Labfiles\Ejercicio 1**, apunta a **ContosoConf.sln**, y luego haz clic en **Abrir**.
>**Nota**: Si aparece el cuadro de diálogo **Aviso de seguridad para ContosoConf**, desactive la casilla **Aviso para cada proyecto de esta solución** y luego haga clic en **OK**.
3.	Expandir el proyecto **ContosoConf**, expandir la carpeta **scripts** y luego expandir la carpeta **pages**.
4.	Haga doble clic en **schedule.js**.
5.	Encuentra el siguiente comentario:

    ```Javascript
        // TODO: Crear una clase de ScheduleList.
    ```
6. Haga clic con el botón derecho del ratón en la carpeta **scripts**, apunte a **Add**, y luego seleccione **JavaScript File**.
7. Para el nombre del elemento, agregue **ScheduleList.js**, y luego haga clic en **Ok**.
8. Añada el siguiente código JavaScript:
	```javascript
		importar { ScheduleItem } de "./ScheduleItem.js";

		exportar la clase ScheduleList {
			//TODO: Añadir Constructor
		}
		
		//TODO: Añadir métodos
	```
9.	En **programa.js**, encuentre y elimine el siguiente comentario:
	```javascript
        // TODO: Crear una clase de ScheduleList.
    ```

#### Tarea 2: Convertir las variables en propiedades de la clase ScheduleList

1.	En **scrodule.js**, encuentra el siguiente comentario:
    ```javascript
        // TODO: Refactoriza estas variables en propiedades de la clase ScheduleList.
		// Asignarlas en el método "inicializar" a partir de los argumentos
    ```
2.	Borre la siguiente línea de código JavaScript después de este comentario:
    ```javascript
        elemento constante, localStarStorage;
    ```

3.	En **ScheduleList.js**, encuentra el siguiente código JavaScript:
    ```javascript
        //TODO: Añadir Constructor
    ```
4.	Reemplaza el código por la siguiente línea de código JavaScript:
    "Javascript
        constructor(elemento, localStarStorage) {
			este.elemento = elemento;
			this.localStarStorage = localStarStorage;
		}
    ```
	
#### Tarea 3: Convertir las funciones en métodos de la clase ScheduleList

1.	En **scrodule.js**, encuentra el siguiente código JavaScript:
    ```javascript
        // TODO: Refactoriza estas funciones en métodos de la clase ScheduleList.
    ```
2.	Borre las funciones **inicioDescarga**, **descargaHecha**, **descargaFallido**, **añadirTodo**, y **añadir** que siguen a este comentario.
3.  En **ScheduleList.js**, encuentra el siguiente comentario:
    ```javascript
        //TODO: Añadir métodos
    ```
3.	Reemplaza el código por el siguiente código JavaScript:
    "Javascript
		async startDownload() {
			// esperar la respuesta de la llamada de búsqueda
			let response = await fetch("/sched/list")
			// transformar el cuerpo en json
			let data = await response.json();
	
			// comprobar la respuesta está bien
			si (respuesta.ok) {
				this.downloadDone(data);
			} más {
				this.downloadFailed();
			}
		}

		downloadDone(responseData) {
			este.addAll(programa.de.datos.de.respuesta);
		}

		downloadFailed() {
			alerta ("No pude recuperar los datos del programa en este momento. Por favor, inténtelo de nuevo más tarde");
		}

		addAll(itemsArray) {
			itemsArray.forEach(esto.agregar, esto);
		}

		add(itemData) {
			const item = nuevo ScheduleItem(itemData, this.localStarStorage);
			this.element.appendChild(item.element);
		}
    ```

#### Tarea 4: Crear y utilizar un objeto ScheduleList

1.	En **scrodule.js**, encuentra el siguiente código JavaScript:
    ```javascript
        // TODO: Reemplaza el siguiente código creando un objeto ScheduleList 
        // y llamando al método startDownload.
        element = document.getElementById("schedule");
        localStarStorage = LocalStarStorage.create(localStorage);
        startDownload();
    ```
2.	Borre este bloque de código JavaScript y reemplácelo por el siguiente código:
    "Javascript
		const scheduleList = new ScheduleList(
			document.getElementById("schedule"),
			nuevo LocalStarStorage(localStorage)
		);
		scheduleList.startDownload();
    ```
3.	Encuentra el siguiente código JavaScript:
    ```javascript
		//Importar objetos/funciones de los módulos/clases.
		importar { LocalStarStorage } de "../LocalStarStorage.js";
		importar { ScheduleItem } de "../ScheduleItem.js";
    ```
4.	Borre este bloque de código JavaScript y reemplácelo por el siguiente código:
    "Javascript
		importar { LocalStarStorage } de "../LocalStarStorage.js";
		importar { ScheduleList } de "../ScheduleList.js";
    ```


#### Tarea 5: Probar la aplicación

1.	En **Solution Explorer**, haga doble clic en **schedule.htm**.
2.	En el menú **Debug**, haga clic en **Start Without Debugging**.
3.	En Microsoft Edge, si la **Configuración de la Intranet está desactivada por defecto** del objeto **ScheduleList** aparece, haga clic en **No mostrar este mensaje de nuevo**.
4.	Verifica que la página se vea similar a la imagen de abajo:

![alt text](./Imágenes/20480B_7_Schedule-Refactored.png "La página del Schedule")

5.	Cerrar Microsoft Edge.
6.      Cierre todas las ventanas abiertas.

>**Resultados**: Al completar este ejercicio, has usado objetos para refactorizar el código JavaScript para que la página **Calendario** sea más mantenible.
Después de completar este ejercicio, habrá refactorizado el código JavaScript para que la página **Calendario** sea más mantenible usando objetos.
