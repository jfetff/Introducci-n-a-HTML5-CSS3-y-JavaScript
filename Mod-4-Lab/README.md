# Module 4 - Lab: Creando formulario para coleccionar y validar las entradas del usuario

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** 24 de Septiembre 2020.
3. **Resumen del Ejercicio:**
    * Modificar la página de registro de los conferenciantes para validar las entradas por cada conferenciantes.
    * El principal objetivo de este laboratorio es modificar la página de registro de la conferencia para validar las entradas de la contraseña, haciendo especialmente en estilos, atributos y contraseñas.
4. **Dificultad o problemas presentados y como se resolvieron:** Ninguna dificultad.

Fecha de entrega: Jueves 24 de septiembre de 2020

>**Objetivos**: 

* Modificar la página de registro de los conferenciantes para validar las entradas por cada conferenciantes.
* El principal objetivo de este laboratorio es modificar la página de registro de la conferencia para validar las entradas de la contraseña, haciendo especialmente en estilos, atributos y contraseñas.

## Lab Pasos

## Ejercicio 1: Creando un Formulario y validar las entradas de los usuarios usando los atributos HTML5

#### Paso 1: Modificar la página de registro

* Abrir Visual Studio 2019
* Crear un nuevo proyecto: **ContosoConf**.

1.	Abrir Microsoft Visual Studio 2019.
2.	Abrir el proyecto dado **\Allfiles\Mod04\Labfiles\Starter\Exercise 1**, clic **ContosoConf.sln** y hacer clic en **Open**
3.	Doble-clic en **schedule.htm**.
4.	En el **Solution Explorer**, expandir el proyecto **ContosoConf**, doble-clic **register.htm**.
5.	Encontrar y revisar el comentario que comient con el siguietne texto:
   ```html
        TODO: Add form inputs
   ```
6.	En el elemento **&lt;head&gt;**, verificar que el siguiente HTML markup esta presente:
   ```html
        <link href="/styles/pages/register.css" rel="stylesheet" type="text/css" />
   ```
7.	Antes de la etiqueta **&lt;/body&gt;** casi al final del archivo, verificar que el siguiente HTML markup esta presente:
   ```html
        <script src="/scripts/pages/register.js" type="text/javascript"></script>
   ```

#### Pasos 2: Agregar los inputs al formulario en la pagina de registro

1.	En el archivo **register.htm**, borrar el siguiente código HTML markup:
   ```html
        <!-- Use the following template for the inputs -->
        <div class="field">
            <label for="{input-id}">label:</label>
            <input type="{type}" id="{input-id}" name="{input-name}" />
        </div>
   ```
2.	En el lugar de lo borrado del paso anterior, agregar el siguiente código HTML markup:
   ```html
        <div class="field">
            <label for="first-name">First name:</label>
            <input type="text" id="first-name" name="FirstName" />
        </div>
        <div class="field">
            <label for="last-name">Last name:</label>
            <input type="text" id="last-name" name="LastName" />
        </div>
        <div class="field">
            <label for="email-address">Email address:</label>
            <input type="email" id="email-address" name="EmailAddress" />
        </div>
        <div class="field">
            <label for="password">Choose a password:</label>
            <input type="password" id="password" name="Password" />
        </div>
        <div class="field">
            <label for="confirm-password">Confirm your password:</label>
            <input type="password" id="confirm-password" name="ConfirmPassword" />
        </div>
        <div class="field">
            <label for="website">Website/blog:</label>
            <input type="url" id="website" name="WebsiteUrl" />
        </div>
   ```
3.	En el menu **Debug**, clic **Start Without Debugging**.
4.	En la caja **First name**, escriba **Josh**.
5.	En la caja **Last name**, escriba **Bailey**.
6.	En la caja **Email address**, escriba **josh.bailey@adatum.com**.
7.	En la caja **Choose a password**, escriba **Passw0rd**.
8.	En la caja **Confirm your password**, escriba **Passw0rd**.
9.	En la caja **Website/blog**, escriba **http://adatum.com/**.
10.	clic **Register**.
11.	Verificar que la aplicación muestra la página **Thanks for registering**.
12.	Regrese a la página **Register**. Note que para poder registrarse tiene que de manera explicita hacer clic y poner el curso en la casilla **First name**. También puede dejar en blanco o escribir cualquier texto sin sentido.
13.	Dejar la casilla vacia, hacer clic **Register**.
14.	Verficar que la aplicación muestra el siguiente mensaje:
   ```html
        Invalid registration information

        The FirstName field is required.
        The LastName field is required.
        The EmailAddress field is required.
        The Password field is required.
        The ConfirmPassword field is required.
   ```
15.	Cerrar el navegador.

#### Pasos 3: Hacer el Formulario más amigable para el usuario

1.	En ContosoConf - Microsoft Visual Studio >> **Solution Explorer**, doble-clic **register.htm**.
2.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="text" id="first-name" name="FirstName" />
   ```
3.	Agregar el atributo **autofocus** que se muestra abajo:
   ```html
        <input type="text" id="first-name" name="FirstName" autofocus="autofocus" />
   ```
4.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="url" id="website" name="WebsiteUrl" />
   ```
5.	Agregar el atributo el atributo del marcador de posición attribute como se muestra:
   ```html
        <input type="url" id="website" name="WebsiteUrl" placeholder="http://" />
   ```
6.	En el menu **Debug**, clic **Start Without DebuggEng**.
7.	En navegador, verificar que el cursor esta ubicado en la casilla de verficiación **First name**.
8.	Verificar que la casilla de verificiación **Website/blog** contiene **http://** texto de marcador de posición.
9.	Cerrar el navegador.

#### Paso 4: Validar los datos mandatorios no encontrados

1.	En **Solution Explorer**, doble-clic **register.htm**.
2.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="text" id="first-name" name="FirstName" autofocus="autofocus" />
   ```
3.	Agregar el atributo the **required** como se muestra abajo:
   ```html
        <input type="text" id="first-name" name="FirstName" required="required" autofocus="autofocus" />
   ```
4.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="text" id="last-name" name="LastName" />
   ```
5.	Agregar el atributo **required**  como se muestra aquí abajo:
   ```html
        <input type="text" id="last-name" name="LastName" required="required" />
   ```
6.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="email" id="email-address" name="EmailAddress" />
   ```
7.	Agregar el atributo **required** como se muestra aquí abajo:
   ```html
        <input type="email" id="email-address" name="EmailAddress" required="required" />
   ```
8.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="password" id="password" name="Password" />
   ```
9.	Agregar el atributo **required** como se muestra aquí abajo:
   ```html
        <input type="password" id="password" name="Password" required="required" />
   ```
10.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="password" id="confirm-password" name="ConfirmPassword" />
   ```
11.	Agregar el atributo **required** como se muestra aquí abajo:
   ```html
        <input type="password" id="confirm-password" name="ConfirmPassword" required="required" />
   ```
12.	En el menu **Debug**, clic **Start Without Debugging**.
13.	En el navegador, clic **Register** sin incluir ningún dato.
14.	Verificar que aplicación sobresalta cada casilla mandatoria y que el formulario muestra el siguiente mensaje de error:
   ```html
        This is a required field
   ```
15.	En la casilla de verificación **First name**, escriba **Josh**.
16.	En la casilla de verificación **Last name**, escriba **Bailey**.
17.	En la casilla de verificación **Email address**, escriba **josh.bailey@adatum.com**.
18.	En la casilla de verificación **Choose a password**, escriba **Passw0rd**.
19.	En la casilla de verificación **Confirm your password**, escriba **Passw0rd**.
20.	En la casilla de verificación **Website/blog**, escriba **http://adatum.com/**.
21.	Clic en **Register** y verificar que **Thanks for registering** aparece en la página.
22.	Cerrar el navegador.

#### Paso 5: Agregar una validación de contraseña compleja

1.	En el **Solution Explorer**, doble-clic **register.htm**.
2.	Encontrar la linea que contiene el siguiente código HTML markup:
   ```html
        <input type="password" id="password" name="Password" required="required"  />
   ```
3.	Agregar lo atributos **pattern** y **title** como se muestra aquí abajo:
   ```html
        <input type="password" id="password" name="Password" required="required" pattern="[a-zA-Z0-9]{5,}" title="At least 5 letters and numbers" />
   ```
4.	En el menu **Debug**, clic **Start Without Debugging**.
5.	En el navegador, en la casilla de verificación **First name**, escriba **Josh**.
6.	En la casilla de verificación **Last name**, escriba **Bailey**.
7.	En la casilla de verificación **Email address**, escriba **josh.bailey@adatum.com**.
8.	En la casilla de verificación **Choose a password**, escriba **abc**.
9.	En la casilla de verificación **Confirm your password**, escriba **abc**.
10.	Clic **Register**.
11.	Verificar que la casilla de verificación **Choose a password** muestra el siguiente mensaje de error:
   ```html
        You must use this format: At least 5 letters and numbers
   ```
12.	En la casilla de verificación **Choose a password**, escriba **Passw0rd**.
13.	En la casilla de verificación **Confirm your password**, escriba **Passw0rd**.
14.	En la casilla de verificación **Website/blog**, escriba **http://adatum.com/**.
15.	Clic en **Register** y verifique que la página **Thanks for registering** page aparecce.
16.	Cerrar navegador.

---
---


## Exercise 2: Validación de la entrada del usuario en JavaScript

#### Paso 1: Escriba código para obtener el contenido de los inputs de contraseña

1.	En ContosoConf - Microsoft Visual Studio, en el menu **File** >> **Open** >> **Project/Solution**.
2.	En la caja de dialogo **Open Project**, ir a **\Allfiles\Mod04\Labfiles\Start\Exercise 2**, clic **ContosoConf.sln**, y clic **Open**.
3.	En el **Solution Explorer**, expandir el proyecto **ContosoConf**, expandir el folder **scripts**, y expandir el folder **pages**.
4.	doble-clic **register.js**.
5.	Encontrar el siguiente comentario:
   ```javascript
        // TODO: Task 1 - Get the password <input> elements from the DOM by ID
   ```
6.	Después del comentario, agrega el siguiente código JavaScript
   ```javascript
        var passwordInput = document.getElementById("password");
        var confirmPasswordInput = document.getElementById("confirm-password");
   ```

#### Paso 2: Escriba un código para comparar las entradas entre **Password** y **Confirm Password**

1.	En el archivo **register.js**, encontrar la siguiente linea de comentario:
   ```javascript
        // TODO: Task 2 - Compare passwordInput value to confirmPasswordInput value
   ```
2.	Después del comentario, agregra el siguiente código JavaScript
   ```javascript
        var passwordsMatch = passwordInput.value === confirmPasswordInput.value;
   ```

#### Paso 3: Escriba el código que muestra un error personalizado de mensaje si las contraseñas son diferentes

1.  En el archivo **register.js**, encontrar el comentario que comienza con las estrellas con el siguiente texto:
   ```javascript
        // TODO: Task 3
   ```
2.	Después de este comentario, agregra el siguiente código JavaScript
   ```javascript
        if (passwordsMatch) {
            // Clear any previous error message.
            confirmPasswordInput.setCustomValidity("");
        } else {
            // Setting this error message will prevent the submission of the form.
            confirmPasswordInput.setCustomValidity("Your passwords don't match. Please escriba the same password again.");
        }
   ```

#### Paso 4: Agregar eventos listeners de entrada a las de llamada del metodo checkPasswords

1.	En el archivo **register.js**, encontrar el comentario que comienza con el siguiente texto:
   ```javascript
        // TODO: Task 4
   ```
2.	Después del comentario, agregra el siguiente código JavaScript
   ```javascript
        passwordInput.addEventListener("input", checkPasswords, false);
        confirmPasswordInput.addEventListener("input", checkPasswords, false);
   ```
3.	En **Solution Explorer**, doble-clic **register.htm**.
4.	En el menu **Debug**, clic **Start Without Debugging**.
5.  En el navegador, nn la casilla de verificación **First name**, escriba **Josh**.
6.  En la casilla  **Last name**, escriba **Bailey**.
7.  En la casilla  **Email address**, escriba **josh.bailey\@adatum.com**.
8.  En la casilla **Choose a password**, escriba **abc123**.
9.  En la casilla **Confirm your password**, escriba **abc456**.
10.  clic **Register**.
11.  Verificar que la casilla **Confirm your password** muestra el siguiente mensaje de error
message:
   ```html
       Your passwords don't match. Please escriba the same password again.
   ```
12.  En la casilla **Confirm your password**, escriba **abc123**.
13.  clic **Register**, verificar que **Thanks for registering** aparace en la página.
14.  Cerrar navegador.

#### Paso 5: Estilizar los elementos que no son válidos

1.	En el proyecto **Solution Explorer**, in the **ContosoConf**, expandir el folder **styles**, y expandir el folder **pages**.
2.	doble-clic **register.css**.
3.	Encontrar el comentario que comienza con el siguiente texto:
   ```css
        /* TODO: Task 5
   ```
4.	Por debajo del comentario, agrega el siguiente estilo:
   ```css
        .register form.submission-attempted input:invalid {
            background-color: #f9b2b2;
            outline: none;
        }
   ```
5.  En **Solution Explorer**, doble-clic **register.htm**.
6.  En el menu **Debug**, clic **Start Without Debugging**.
7.  En el navegador, clic **Register**.
8.  Verificar que la aplicación resalta las casillas **First name**, **Last name**, **Email address**, **Choose a password**, y **Confirm your password** con fondos de color.
9.  Cerrar navegador.
10. Cerrar todo.