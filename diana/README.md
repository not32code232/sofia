### DIANA BOT DOCUMENTACION

<hr>

### INDICE

- [COMANDOS ADMINISTRADOR](#comandos-administrador)
- [IDENTIFICAR ERRORES Y REPORTE](#identificar-errores-y-reporte)
- [PROCESO LEVANTAR Y CORRER PROYECTO](#proceso-levantar-y-correr-proyecto)

<hr>

### STACK TECNOLOGICO

El proyecto se construye utilizando las siguientes tecnologías:

- [Python](https://www.python.org/)
- [Selenium](https://www.selenium.dev/)
- [PyAutoGUI](https://pypi.org/project/PyAutoGUI/)
- [XAMPP](https://www.apachefriends.org/index.html)
- [MySQL](https://www.mysql.com/)
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)

Conociendo las bases de cada una de estas podremos desarrollar, corregir o modificar el mismo con mayor entendimiento. Para este entendimiento se debe tener en cuenta el flujo general.

<hr>

### COMANDOS ADMINISTRADOR

**Aclaraciones:**

Las palabras en negrita son palabras clave, por ende SIEMPRE se envían igual al momento de realizar el comando.
Las palabras subrayadas NO siempre se envían igual, esto depende de la ocasión.
Cuando el administrador envíe un comando SIEMPRE espere una respuesta antes de enviar otro.

**Comandos:**

- Carga:

Cancelar carga: <code>**Carga** + número de operación + cancelar</code>

Carga recibida: <code>**Carga** + número de operación + recibido + monto</code>

- Descarga:

Cancelar descarga: <code>**Descarga** + número de operación + cancelar</code>

Descarga transferida: <code>**Descarga** + número de operación + transferido</code>

- Consultar fichas en panel de administrador: <code>**Fichas panel**</code>

- Cambiar datos bancarios para pasos de transferencia: <code>**Banco** + cbu + alias + nombre de cuenta</code>

<hr>

### IDENTIFICAR ERRORES Y REPORTE

Este apartado ha sido simplificado de manera que se puedan identificar de manera rápida y efectiva los errores y ver el estado del software accediendo al canal de WhatsApp en el cual Sofia enviará estas alertas.

**Funcionalidad y uso:**

Sofia a medida que va realizando sus acciones, desde leer el chat, hasta cumplir con lo que el jugador o administrador solicitó, cada que ingresa a una nueva funcionalidad va registrando en que proceso / funcionalidad se encuentra. Si en el mismo proceso ha sucedido algún tipo de error, se registra este y se devuelve una alerta en el canal de WhatsApp dando aviso y el detalle de cuál fue el último proceso que se realizó para poder ubicarlo dentro del código mediante via email (para mayor organización) y realizar correcciones de ser necesarias.

Si deseamos corregir algún error o simplemente acceder al código para verificar su funcionamiento o causa del error, debemos abrir nuestro proyecto en el editor de preferencia y buscar en el proyecto el nombre de la función o linea que ha generado ese error, el cual nos llevara a donde se encuentra toda la lógica de ese proceso y verificar o corregir lo que debamos.

<hr>

### PROCESO LEVANTAR Y CORRER PROYECTO

**Requerimientos previos para iniciar:**

1. Servidor VPS con un mínimo de 16 GB de RAM con sistema operativo Windows Server 2022.
2. Tener el código fuente del proyecto listo para importar o descargar.

**Paso a paso:**

1. Instalar en la máquina la última versión de Python (https://www.python.org/downloads/). Al momento de instalar debemos verificar que tengamos checkeado la opción <code>Add python.exe to PATH</code> para que esto pueda funcionar de forma correcta.

<img width="500" alt="Screenshot 2023-07-15 at 16 15 43" src="https://github.com/not32code232/sofia/assets/134972894/99cb100c-1d23-4039-856e-73b2d45f70da">

2. Abrimos la terminal de nuestro equipo y en la carpeta raíz correremos el siguiente comando para instalar las dependencias necesarias: primero ejecutamos <code>pip install pip</code> y luego <code>pip install selenium pandas numpy mysql-connector-python unidecode pyautogui</code>.

3. Descomprimimos nuestra carpeta del proyecto dejándola disponible en escritorio para facilitar el acceso.

4. Configuramos datos iniciales:

Para poder iniciar el proyecto correctamente, previamente necesitamos de ciertos datos iniciales los cuales agregaremos en el archivo que se encuentra dentro del proyecto con el nombre <code>config.py</code> donde veremos lo siguiente y completaremos con nuestros datos aquello que se nos pide en este archivo:

- Numero superadministrador.
- Usuario y contrasena panel plataforma.
- Nombre de bot.
- Datos de transferencia.
- URL de la plataforma.
- CBU de cuenta a transferir.
- Alias de cuenta a transferir.
- Nombre de cuenta a transferir.
- User config (solo gama planeta, este nombre de usuario debe comenzar con la letra A, **este usuario deberá ser creado si no existe uno que inicie con la letra A**)

Ejemplo de <code>config.py</code> a continuacion:

<img width="500" src="https://github.com/not32code232/sofia/assets/134972894/147bb3ca-23a6-417c-a79d-024ab6a4d632"><br>

Como ultimo dato de configuración inicial se debe agregar el número de ADMINISTRADOR dentro del archivo <code>contactos_autorizados.txt</code> dentro de la carpeta <code>resource</code> del proyecto tal cual como figura en WhatsApp, ejemplo abajo.

<img width="400" alt="Screenshot 2023-07-09 at 12 02 28" src="https://github.com/not32code232/sofia/assets/134972894/2c866001-27d9-44ae-be78-6af9302707c0">

5. Descargamos de la siguiente dirección [Apache Friends](https://www.apachefriends.org/index.html) la última versión de XAMPP para windows, esto nos permitirá tener nuestra base de datos corriendo.

<img width="500" alt="Screenshot 2023-06-05 at 22 40 51" src="https://github.com/not32code232/sofia/assets/134972894/b0a8ae7a-c9f0-4d2f-90ad-6841f7e9a806"><br>

6. Una vez instalado XAMPP lo iniciamos y damos a <code>start</code> a <code>Apache</code> y <code>MySQL</code>.

<img width="500" alt="Screenshot 2023-06-06 at 10 33 55" src="https://github.com/not32code232/sofia/assets/134972894/fcf8f289-9f7a-4907-8df4-fb56f1017e3c"><br>

7. Ingresamos dentro del navegador a la ruta <code>localhost/phpmyadmin</code> (o ingresando directamente a <code>localhost</code> y buscando la sección de <code>phpmyadmin</code>) en donde nos llevará al panel de administrador de la base de datos PHP.

Deberemos crear una nueva tabla con el nombre <code>sofia.chat</code>, luego de eso importamos el archivo que se encuentra dentro de la carpeta <code>resource</code> con la extensión de <code>.sql</code>.

<img width="500" alt="Screenshot 2023-06-06 at 10 45 14" src="https://github.com/not32code232/sofia/assets/134972894/2a443d11-e2a8-4ec8-8b00-a2417ea9697b"><br>

**IMPORTANTE:** En lo que respecta a la importación que realizamos hacia la base de datos, este proceso se realizará una sola vez. Luego de esta importación podremos frenar y volver a iniciar la base de datos sin problema **pero no volver a importar la colección** ya que si realizamos esto perderemos todos nuestros datos.

8. Descargar e instalar el navegador Microsoft Edge ([Download Microsoft Edge](https://www.microsoft.com/en-us/edge/download)).

<img width="500" alt="Screenshot 2023-06-06 at 08 41 00" src="https://github.com/not32code232/sofia/assets/134972894/5ef2eddd-e636-4969-9ebf-421608e1a0bd"><br>

9. Descargar e instalar el navegador Google Chrome ([Google Chrome - Download the Fast, Secure Browser from Google](https://www.google.com/chrome/)).

10. Descargar Web Driver para Edge validando la versión y descargando el correspondiente a la misma, instructivo a detalle en página oficial: [Edge Webdriver](https://learn.microsoft.com/en-us/microsoft-edge/webdriver-chromium/?tabs=c-sharp#download-microsoft-edge-webdriver).

11. Descargar Web Driver para Chrome validando la versión y descargando el correspondiente a la misma en [ChromeDriver](https://chromedriver.chromium.org/downloads), descargando la versión de windows disponible. Es importante validar su versión en ambos navegadores, esta información la veremos en detalles del navegador.

<img width="500" alt="Screenshot 2023-06-06 at 08 43 06" src="https://github.com/not32code232/sofia/assets/134972894/44aab0f6-33b6-4fc2-ac00-bc078172f4f9"><br>

<img width="500" alt="Screenshot 2023-06-06 at 08 43 55" src="https://github.com/not32code232/sofia/assets/134972894/bdfb25bd-dcc1-4798-afe6-2f3a5a1f96dc"><br>

12. Una vez descargados los drivers los ubicamos a ambos en la carpeta <code>driver</code> del proyecto, cada uno con su nombre <code>chromedriver</code> y <code>edgedriver</code>.

13. Para que el bot de avisos a los canales, deberemos crearlos de forma manual, en este canal debe ser miembro el numero que se posee el bot y el administrador.
    
- Creamos los grupos desde el número que posee el bot tal cual describimos abajo.
- Agregamos como miembro al administrador.
- Configuramos en el grupo que solo puede enviar mensajes el creador del mismo, o sea el bot.
- Silenciamos el grupo de reportes para que no interrumpa al administrador ya que este solo es de lectura.

Los grupos a crear son los siguientes:

- SOLICITUD DE CARGA
- SOLICITUD DE DESCARGA
- SOLICITUD ATENCION AL CLINETE
- SOFIA REPORTES

**IMPORTANTE**, la creación de estos grupos deberá ser tal cual se describen.

14. Abrimos una nueva consola (terminal) ubicándonos nuevamente en la raíz del proyecto y corremos el archivo <code>supermain.py</code> con el comando <code>python supermain.py</code>.

Al ejecutar este archivo se nos abrirán dos navegadores, uno por vez, en donde nos pedirá escanear el QR de WhatsApp para ingresar con el número que corresponde, cuando escaneamos el mismo, volveremos a la consola a presionar ENTER para continuar con el siguiente navegador, escanear el QR y nuevamente presionar ENTER dando paso a la apertura de la plataforma.

**GAMA PULPOBET:**

Abierta la ventana con la plataforma una vez ejecutado <code>supermain.py</code>, deberemos realizar lo siguiente:

- En la parte superior donde vemos las páginas, seleccionar modo vista con la mayor cantidad disponible, ejemplo 50.
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- Dejamos en primer plano esta ventana en pantalla completa.
- Controlamos de tener habilitado el "Incluir Bloqueados".

Quedandonos con una vista de la siguiente forma:

<img width="500" alt="Screenshot 2023-06-06 at 10 58 21" src="https://github.com/not32code232/sofia/assets/134972894/9acd94a5-fb1d-46c7-a7fd-f8185af1b911"><br>

**GAMA PLANETA:**

- Todos los paneles de la gama de planeta, debe que existir un usuario que empiece con la letra A (para que este al principio) y tiene que cargarse al config.py en la variable user_config. **DE NO EXISTIR USUARIO QUE COMIENCE CON LETRA "A", SE DEBERA CREAR UNO**.
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- **IMPORTANTE**, en esta gama NO debe haber agentes en el panel, solo debe haber jugadores, si este tiene agentes puede no funcionar.

**GAMA JUGALO:**
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- Seleccionar si no lo esta, el boton "Todos" en el area de la tabla de usuarios.

15. ¡Listo para trabajar! Ahora solo queda hacer unas breves pruebas para comprobar que todo esté correctamente funcionando y ya podemos dejarlo corriendo. De lo contrario deberemos volver a los pasos o identificar el error para hacerlo que funcione.
