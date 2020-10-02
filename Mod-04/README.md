# Módulo 5: Creación de formularios para recoger y validar las entradas de los usuarios

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

Dondequiera que la ruta de un archivo comience con *[Raíz del repositorio]*, reemplácela con la ruta absoluta de la carpeta en la que reside el repositorio 20480. Por ejemplo, si clonaste o extrajiste el repositorio 20480 a **C:\Usuarios\John Doe\Descargas\20480**, cambia la ruta: **[Raíz del Repositorio]\N-Todos los Archivos 20480CMod01** a **C:\N-Usuarios John Doe\N-Descargas 20480\N-Todos los Archivos 20480CMod01**.

## Lección 3: Validar la entrada del usuario usando JavaScript.

### Demostración: Creación de un formulario y validación de los datos del usuario

#### Pasos de preparación 

Asegúrate de que has clonado el directorio 20480C de GitHub (**https://github.com/MicrosoftLearning/20480-Programming-in-HTML5-with-JavaScript-and-CSS3/tree/master/Allfiles**). Contiene los segmentos de código para los laboratorios y demostraciones de este curso.

#### Pasos de la demostración


1. Lea el escenario del laboratorio a los estudiantes y señale que deben leer cada escenario antes de intentar el laboratorio para un módulo.
2. Señale a los estudiantes que el escenario del ejercicio para cada ejercicio es una lectura esencial y contiene una descripción de lo que lograrán en el ejercicio.
3. Inicie Microsoft Visual Studio. Desde la carpeta ** [Repository Root] \ Allfiles \ Mod04 \ Labfiles \ Solution \ Exercise 2 **, abra la solución ** ContosoConf.sln **.
> ** Nota **: Si aparece el cuadro de diálogo ** Advertencia de seguridad para ContosoConf **, desactive la casilla de verificación ** Preguntarme por todos los proyectos de esta solución ** y luego haga clic en ** Aceptar **.
4. En ** Explorador de soluciones **, expanda el proyecto ** ContosoConf ** y luego haga doble clic en ** register.htm **.
5.	En la ventana **Editorial de códigos**, busque el elemento **&lt;form El formulario contiene casillas para el nombre, el apellido, la dirección de correo electrónico, la contraseña (incluida una casilla de confirmación de la contraseña) y una dirección URL opcional, si el usuario tiene un sitio web. El marcado HTML utiliza atributos de entrada para validar los datos introducidos por el usuario.
6.	En **Solution Explorer**, expande la carpeta **scripts**, expande la carpeta **pages**, y luego haz doble clic en **register.js**.
7. En la ventana **Editorial de códigos**, explique que los estudiantes escribirán la función **marcarContraseña** para verificar que los valores introducidos en las casillas **Contraseña** y **Confirmar Contraseña** coincidan.
8.	En **Solution Explorer**, expande la carpeta **styles**, expande la carpeta **pages**, y luego haz doble clic en **register.css**.
9.	En la ventana **Editorial de Códigos**, explique que los estudiantes crearán el estilo que resalte los elementos de entrada que no pasen la validación usando la seudo-clase **input:invalid**.
10. En el menú **Debug**, haga clic en **Iniciar sin depuración**.
11.	En Microsoft Edge, en la página de **Home**, en la barra de navegación, haga clic en **Register**.
12.	En la página **Registrarse**, haga clic en **Registrarse**, y señale que el formulario no permite al usuario omitir información obligatoria, como el nombre, el apellido, la dirección de correo electrónico o la contraseña.
13.	En la casilla **Nombre**, escriba **Josh**.
14.	En la casilla **Apellido**, escriba **Bailey**.
15.	En la casilla **Dirección de correo electrónico**, escriba **josh.bailey@adatum.com**.
16.	En la casilla **Seleccione una contraseña**, escriba **Passw0rd**.
17.	En la casilla **Confirme su contraseña**, escriba **Passw0rd**.
18.	En la casilla **Sitio web/blog**, escriba **http://adatum.com/**.
19. Haga clic en **Registrarse** y verifique que aparezca la página **Gracias por registrarse**.
20.	Mencione que el formulario también realiza otras comprobaciones, como verificar que la dirección de correo electrónico esté en el formato correcto, y que los valores de los campos de contraseña y contraseña de confirmación coincidan.
21.	Cierre el navegador.
22. Cierre todas las ventanas abiertas.