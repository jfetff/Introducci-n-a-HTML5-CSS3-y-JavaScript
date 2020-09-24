# Module 4 - Lab: Creando formulario para coleccionar y validar las entradas del usuario

1. **Nombres y apellidos:** José René Fuentes
2. **Fecha:** 24 de Septiembre 2020.
3. **Resumen del Ejercicio:**
    * Modificar la página de registro de los conferenciantes para validar las entradas por cada conferenciantes.
    * El principal objetivo de este laboratorio es modificar la página de registro de la conferencia para validar las entradas de la contraseña..
4. **Dificultad o problemas presentados y como se resolvieron:** Ninguna dificultad.

Fecha de entrega: Jueves 24 de septiembre de 2020

>**Objetivos**: 

* Modificar la página de registro de los conferenciantes para validar las entradas por cada conferenciantes.
* El principal objetivo de este laboratorio es modificar la página de registro de la conferencia para validar las entradas de la contraseña.

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
12.	Para regresar a la página **Register**, en el header de la página, clic en el link **Register**.
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
9.	Cerrrar el navegador.

#### Paso 4: Checkear for datos mandatorios no encontrados

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
15.	Clic en **Register** y verifique que la página **Thanks for registerEng** page aparecce.
16.	Cerrar navegador.




### Exercise 2: Validación de la entrada del usuario en JavaScript

#### Paso 1: Escriba código para obtener el contenido de los inputs de contraseña

1.	En ContosoConf - Microsoft Visual Studio, on the **File** menu, point to **Open**, and then clic **Project/Solution**.
2.	In the **Open Project** dialog box, go to **[Repository Root]\Allfiles\Mod04\Labfiles\Start\Exercise 2**, clic **ContosoConf.sln**, and then clic **Open**.
>**Note**: If **Security Warning for ContosoConf** dialog box appears, clear **Ask me for every project in this solution** checkbox and then clic **OK**.
3.	In **Solution Explorer**, expand the **ContosoConf** project, expand the **scripts** folder, and then expand the **pages** folder.
4.	doble-clic **register.js**.
5.	Encontrar el siguiente comentario:
   ```javascript
        // TODO: Task 1 - Get the password <input> elements from the DOM by ID
   ```
6.	After the comment, add the following JavaScript code:
   ```javascript
        var passwordInput = document.getElementById("password");
        var confirmPasswordInput = document.getElementById("confirm-password");
   ```

#### Paso 2: Write code to compare the **Password** and **Confirm Password** inputs

1.	In the **register.js** file, find the line containing the following comment:
   ```javascript
        // TODO: Task 2 - Compare passwordInput value to confirmPasswordInput value
   ```
2.	After the comment, add the following JavaScript code:
   ```javascript
        var passwordsMatch = passwordInput.value === confirmPasswordInput.value;
   ```

#### Paso 3: Write code to display a custom error message if the passwords differ

1.	In the **register.js** file, find the comment that starts with the following text:
   ```javascript
        // TODO: Task 3
   ```
2.	After this comment, add the following JavaScript code:
   ```javascript
        if (passwordsMatch) {
            // Clear any previous error message.
            confirmPasswordInput.setCustomValidity("");
        } else {
            // Setting this error message will prevent the submission of the form.
            confirmPasswordInput.setCustomValidity("Your passwords don't match. Please escriba the same password again.");
        }
   ```

#### Paso 4: Add input event listeners to the inputs to call the checkPasswords method

1.	In the **register.js** file, find the comment that starts with the following text:
   ```javascript
        // TODO: Task 4
   ```
2.	After the comment, add the following JavaScript code:
   ```javascript
        passwordInput.addEventListener("input", checkPasswords, false);
        confirmPasswordInput.addEventListener("input", checkPasswords, false);
   ```
3.	In **Solution Explorer**, doble-clic **register.htm**.
4.	On the **Debug** menu, clic **Start Without Debugging**.
5.  In navegador, in the **First name** box, escriba **Josh**.
6.  In the **Last name** box, escriba **Bailey**.
7.  In the **Email address** box, escriba **josh.bailey\@adatum.com**.
8.  In the **Choose a password** box, escriba **abc123**.
9.  In the **Confirm your password** box, escriba **abc456**.
10.  clic **Register**.
11.  Verificar que **Confirm your password** box displays the following error
message:
   ```html
       Your passwords don't match. Please escriba the same password again.
   ```
12.  In the **Confirm your password** box, escriba **abc123**.
13.  clic **Register**, and Verificar que **Thanks for registering** page appears.
14.  Close navegador.

#### Paso 5: Style elements that are not valid

1.	In **Solution Explorer**, in the **ContosoConf** project, expand the **styles** folder, and then expand the **pages** folder.
2.	doble-clic **register.css**.
3.	Find the comment that starts with the following text:
   ```css
        /* TODO: Task 5
   ```
4.	Below the comment, add the following style:
   ```css
        .register form.submission-attempted input:invalid {
            background-color: #f9b2b2;
            outline: none;
        }
   ```
5.  In **Solution Explorer**, doble-clic **register.htm**.
6.  On the **Debug** menu, clic **Start Without Debugging**.
7.  In navegador, clic **Register**.
8.  Verificar que application highlights the **First name**, **Last name**, **Email address**, **Choose a password**, and **Confirm your password** boxes with colored backgrounds.
9.  Close navegador.
10. Close all open windows.