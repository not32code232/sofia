### SOFIA BOT DOC

<hr>

### SOLUCION

Automatizar el proceso que se realiza entre el jugador, cajero y plataforma acelerando los tiempos de respuesta y eliminando la interacción por parte del cajero al máximo nivel.

<hr>

### INDICE

- [FLUJO COMPLETO](#flujo-completo)
- [STACK TECNOLOGICO](#stack-tecnologico)
- [COMANDOS SUPERADMINISTRADOR](#comandos-superadministrador)
- [ROL SUPERADMINISTRADOR / PROPIETARIO](#rol-superadministrador--propietario)
- [COMANDOS ADMINISTRADOR](#comandos-administrador)
- [ROL ADMINISTRADOR](#rol-administrador)
- [IDENTIFICAR ERRORES Y REPORTE](#identificar-errores-y-reporte)
- [PERSONALIZACION DE MENSAJES](#personalizacion-de-mensajes)
- [ACTUALIZAR CLASES WHATSAPP](#actualizar-clases-whatsapp)
- [PROCESO LEVANTAR Y CORRER PROYECTO](#proceso-levantar-y-correr-proyecto)


<hr>

### FLUJO COMPLETO

![flujoCompletoSofia drawio](https://github.com/not32code232/sofia/assets/134972894/e1546c28-b116-40fd-9b27-f3abf3103310)

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

### COMANDOS SUPERADMINISTRADOR

**Recordemos** que el SUPERADMINISTRADOR es el propietario del proyecto.

**Comandos:**

- Cambiar número administrador: <code>Admin + MUNERO DE WHATSAPP</code> un ejemplo de uson sería el siguiente <code>Admin +54 9 3523 41-1111</code>. El número que coloquemos **deberá escribirse TAL CUAL** figura el mismo en WhatsApp, incluyendo el signo más (+), los espacios y el guión.

<hr>

### ROL SUPERADMINISTRADOR / PROPIETARIO

El rol del propietario se define por sus tareas y responsabilidades las cuales son:
- Configurar el entorno de trabajo. 
- Delegrar y controlar los permisos de inicio para Administrador.

El propietario, a su vez posee comandos de **SUPERADMINISTRADOR y ADMINSTRADOR** para poder realizar y cumplir con sus responsbilidades sin restricciones por parte del software.

Detalles de como hacer esto en [PROCESO LEVANTAR Y CORRER PROYECTO](#proceso-levantar-y-correr-proyecto).

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

### ROL ADMINISTRADOR

El rol del administrador se define por sus tareas y responsabilidades las cuales son:
- Confirmar cargas.
- Confirmar descargas.
- Atención al cliente.
- Acceso a reportes.

Cada una de estas responsabilidades corresponde a un canal en donde Sofia enviara mensajes dando aviso, estos canales son solo de lectura, para confirmar o realizar alguna acción con respecto a estos canales de avisos, **se deberá comunicar con Sofia utilizando los [COMANDOS ADMINISTRADOR](#comandos-administrador)**.

Las vistas de los canales serán del tipo:

- Confirmar cargas:

<img width="320" alt="Screenshot 2023-06-06 at 09 02 30" src="https://github.com/not32code232/sofia/assets/134972894/7680b729-f01a-4b1e-a2db-22389e27e523"><br>

- Confirmar descargas:

<img width="320" alt="Screenshot 2023-06-06 at 09 05 17" src="https://github.com/not32code232/sofia/assets/134972894/84265f0c-0f97-40b7-8d9c-0fffa35ad5bc"><br>

- Atención al cliente:

<img width="320" alt="Screenshot 2023-06-06 at 09 04 32" src="https://github.com/not32code232/sofia/assets/134972894/d1391f19-bce3-40da-aab1-7d5d8e0e56db"><br>

- Acceso a reportes:

<img width="320" alt="Screenshot 2023-06-06 at 09 06 25" src="https://github.com/not32code232/sofia/assets/134972894/4004e8e2-4aef-42b7-89a4-0770bf72faff"><br>

<hr>

### IDENTIFICAR ERRORES Y REPORTE

Este apartado ha sido simplificado de manera que se puedan identificar de manera rápida y efectiva los errores y ver el estado del software accediendo al canal de WhatsApp en el cual Sofía enviará estos reportes.

**Funcionalidad y uso:**

Sofia a medida que va realizando sus acciones, desde leer el chat, hasta cumplir con lo que el jugador o administrador solicitó, cada que ingresa a una nueva funcionalidad va registrando en que proceso / funcionalidad se encuentra. Si en el mismo proceso ha sucedido algún tipo de error, se registra este y se devuelve en el canal de WhatsApp con el detalle de cuál fue el último proceso que se realizó para poder ubicarlo dentro del código y realizar correcciones de ser necesarias.

Si deseamos corregir algún error o simplemente acceder al código para verificar su funcionamiento o causa del error, debemos abrir nuestro proyecto en el editor de preferencia y buscar en el proyecto el nombre de la función que ha generado ese error, el cual nos llevara a donde se encuentra toda la lógica de ese proceso y verificar o corregir lo que debamos.

<hr>

### PERSONALIZACION DE MENSAJES

Si deseamos personalizar uno o varios mensajes que realiza el software deberemos modificar estos directamente desde su código fuente. A continuación los pasos:

1. En el caso de que tengamos el proyecto sin funcionar ni corriendo en su entorno, omitiremos este punto. De lo contrario si tenemos el proyecto funcionando deberemos finalizar todos los procesos **menos la base de datos**, a esto nos referimos con los procesos que tengamos corriendo como los <code>keepSession's</code> y <code>superMain</code>.

3. Una vez finalizado todo los procesos menos el de la base de datos, deberemos ingresar en nuestra carpeta donde se aloja todo el código del proyecto y abrir el archivo <code>msjs.py</code>.

5. En este archivo se encontrarán todos los mensajes que envía el software, para ubicar el que queremos modificar simplemente lo buscaremos en base al texto que tiene este.

7. A la hora de editar solo lo haremos dentro de los **strings** ("") y **no** modificaremos nada aquello que se encuentre entre corchetes ({}), ejemplo <code>{fichas_a_retirar}</code> en donde en el se colocaran los datos que necesitamos mostrar, en el caso ejemplo, se mostrará dependiendo del caso, la cantidad de fichas por retirar. 

Recordemos que podemos agregar negritas en nuestros mensajes con el doble asterisco entre la palabra u oración que deseemos hacerlo, ejemplo " ** texto en negrita ** ".

**NO** está permitido usar emojis en estos mensajes, los mismos no funcionarán cuando se envíen estos.

<hr>

### ACTUALIZAR CLASES WHATSAPP

<hr>

### PROCESO LEVANTAR Y CORRER PROYECTO

**Requerimientos previos para iniciar:**

1. Servidor VPS con un mínimo de 16 GB de RAM con sistema operativo Windows Server 2022.
2. Tener el código fuente del proyecto listo para importar o descargar.

**Paso a paso:**

1. Instalar en la máquina la última versión de Python (https://www.python.org/downloads/).

2. Abrimos la terminal de nuestro equipo y en la carpeta raíz correremos el siguiente comando para instalar las dependencias necesarias: <code>pip install selenium pandas numpy mysql-connector-python unidecode pyautogui</code>.

3. Descomprimimos nuestra carpeta del proyecto dejándola disponible en escritorio para facilitar el acceso.

4. **<p style="color:red;">Configuramos datos iniciales:</p>** ------------------------------------------

Para poder iniciar el proyecto correctamente, previamente necesitamos de ciertos datos iniciales los cuales agregaremos en el archivo que se encuentra dentro del proyecto con el nombre <code>config.py</code> donde veremos lo siguiente y **completaremos con nuestros datos aquello que se encuentre en negritas**:

- num administrador
- num superadministrador
- usuario y contrasena panel plataforma
- nombre de bot
- datos de transferencia

5. Descargamos de la siguiente dirección [Apache Friends](https://www.apachefriends.org/index.html) la última versión de XAMPP para windows, esto nos permitirá tener nuestra base de datos corriendo.

<img width="500" alt="Screenshot 2023-06-05 at 22 40 51" src="https://github.com/not32code232/sofia/assets/134972894/b0a8ae7a-c9f0-4d2f-90ad-6841f7e9a806"><br>

6. Una vez instalado XAMPP lo iniciamos y damos a <code>start</code> a <code>Apache</code> y <code>MySQL</code>.

<img width="500" alt="Screenshot 2023-06-06 at 10 33 55" src="https://github.com/not32code232/sofia/assets/134972894/fcf8f289-9f7a-4907-8df4-fb56f1017e3c"><br>

7. Ingresamos dentro del navegador a la ruta <code>localhost/phpmyadmin</code> en donde nos llevará al panel de administrador de la base de datos PHP, en esta deberemos importar el archivo que se encuentra dentro de la carpeta <code>resource</code> con la extensión de <code>.sql</code>.

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

13. Abrir la terminal (cmd) y ubicarnos en la carpeta base donde tenemos el proyecto y correr el archivo <code>KeepSession.py</code> con el comando <code>python KeepSession.py</code>, esperamos a que se nos abra el Chrome y se cargue WhatsApp Web en donde tendremos que escanear para poder ingresar con el número que será el que reciba a los jugadores, administradores y envíe informes. 
Es importante que NO cerremos la consola el cual corrimos ese comando y NO cancelamos el proceso. Una vez ingresado nuestro WhatsApp, dejar así tal cual sin tocar nada más ni ingresar a ningún chat.

14. Repetimos el paso anterior solo que en vez de con el archivo <code>KeepSession.py</code>, será con el archivo <code>KeepSessionEdge.py</code> corriendo el comando <code>python KeepSessionEdge.py</code>. 

<i>Es importante que NO cerremos la consola el cual corrimos ese comando y NO cancelamos el proceso.</i>

**CASO PULPOBET:**

15. Abrimos una nueva consola (terminal) ubicándonos nuevamente en la raíz del proyecto y corremos el archivo <code>main.py</code> con el comando <code>python main.py</code>. Con este se nos abrirá una ventana con la plataforma donde deberemos realizar lo siguiente:

- En la parte superior donde vemos las páginas, seleccionar modo vista con la mayor cantidad disponible, ejemplo 50.
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- Dejamos en primer plano esta ventana en pantalla completa.

Quedandonos con una vista de la siguiente forma:

<img width="500" alt="Screenshot 2023-06-06 at 10 58 21" src="https://github.com/not32code232/sofia/assets/134972894/9acd94a5-fb1d-46c7-a7fd-f8185af1b911"><br>

16. ¡Listo para trabajar! Ahora solo queda hacer unas breves pruebas para comprobar que todo esté correctamente funcionando y ya podemos dejarlo corriendo. De lo contrario deberemos volver a los pasos o identificar el error para hacerlo que funcione.
