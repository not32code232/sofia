### SOFIA BOT DOC

<hr>

### SOLUCION

Automatizar el proceso que se realiza entre el jugador, cajero y plataforma acelerando los tiempos de respuesta y eliminando la interacción por parte del cajero al máximo nivel.

<hr>

### INDICE

- [FLUJO COMPLETO](#flujo-completo)
- [STACK TECNOLOGICO](#stack-tecnologico)
- [OBSERVACIONES Y RECOMENDACIONES](#observaciones-y-recomendaciones)
- [COMANDOS SUPERADMINISTRADOR](#comandos-superadministrador)
- [ROL SUPERADMINISTRADOR / PROPIETARIO](#rol-superadministrador--propietario)
- [COMANDOS ADMINISTRADOR](#comandos-administrador)
- [ROL ADMINISTRADOR](#rol-administrador)
- [IDENTIFICAR ERRORES Y REPORTE](#identificar-errores-y-reporte)
- [PERSONALIZACION DE MENSAJES](#personalizacion-de-mensajes)
- [SOLUCION ELEMENTO NO ENCONTRADO](#solucion-elemento-no-encontrado)
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

### OBSERVACIONES Y RECOMENDACIONES

El bot fue desarrollado desde un principio para que funcione en en UN SOLO PANEL con UNA SOLA BASE DE DATOS y UN SOLO NÚMERO DE WHATSAPP, todo corriendo y funcionando en UN SOLO SERVIDOR.
Esto mismo debido a las siguientes razones: 
- Seguridad, al tener diversificado cada cliente que use el bot en un solo servidor, con su propia base de datos y su propio número de teléfono, se minimiza al máximo el riesgo extendido. Es decir, si existe algún tipo de problema externo, se da de baja el servidor, número, y base de datos afectado, y listo. Este no afecta a la red de jugadores que se posea ya que funciona sólo como un asistente, y se puede volver a levantar sin problemas en otro servidor, con otra base de datos, otro número de teléfono y el mismo panel de plataforma. Sin mayores inconvenientes, aunque cabe aclarar de que si no se hizo una copia de la base de datos antes de llevarlo o moverlo a otro servidor estos datos se perderán ya que estos solo se encuentran en el mismo server, la solución a esto es de que antes de dar de baja o borrar, se debe hacer una copia de la base de datos de forma manual.
- Su diseño está hecho para que corra UN solo bot (no más de uno) en un mismo servidor, con un número de teléfono y una base de datos. Si se corren más de un bot, puede ser que funcione sin problemas, pero es muy probable que aparezcan errores inesperados y el funcionamiento del mismo se rompa.

A cada cliente que se le venda el servicio del bot, se le debe contratar un servidor propio, que contenga su propia base de datos, y se vincule al número de whatsapp proporcionado por el mismo cliente. De esta forma, se aseguran de que el bot va a correr de forma óptima, y que exista una independencia total entre clientes, lo que hará mucho más fácil el control y administración del servicio. El número de Whatsapp será proporcionado por el cliente, y el servidor, base de datos y panel por el dueño del bot. De esta forma se tendrá un control total sobre los movimientos realizados en el mismo, y sobre todo el código fuente que deberá estar corriendo en la consola del servidor.

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

Este apartado ha sido simplificado de manera que se puedan identificar de manera rápida y efectiva los errores y ver el estado del software accediendo al canal de WhatsApp en el cual Sofia enviará estas alertas. Los detalles de error y procesos de harán via email para mayor organización y proligidad.

**Funcionalidad y uso:**

Sofia a medida que va realizando sus acciones, desde leer el chat, hasta cumplir con lo que el jugador o administrador solicitó, cada que ingresa a una nueva funcionalidad va registrando en que proceso / funcionalidad se encuentra. Si en el mismo proceso ha sucedido algún tipo de error, se registra este y se devuelve una alerta en el canal de WhatsApp dando aviso y el detalle de cuál fue el último proceso que se realizó para poder ubicarlo dentro del código mediante via email (para mayor organización) y realizar correcciones de ser necesarias.

Si deseamos corregir algún error o simplemente acceder al código para verificar su funcionamiento o causa del error, debemos abrir nuestro proyecto en el editor de preferencia y buscar en el proyecto el nombre de la función o linea que ha generado ese error, el cual nos llevara a donde se encuentra toda la lógica de ese proceso y verificar o corregir lo que debamos.

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

### SOLUCION ELEMENTO NO ENCONTRADO

**Aclaracion**
Estas causas de error siempre provienen por el cambio de nombre de un elemento o modificación del mismo, ya sea desde la plataforma o del mismo WhatsApp web. 

Este tipo de error puede llevar a dos causas:

1 - Que WhatsApp haya cambiado sus clases en las cuales Sofía toma para ubicar los elementos desde el navegador.
**Este error lo podemos identificar fácilmente** ya que cada vez que Sofia quiera acceder o leer los nuevos mensajes tendremos este error **de forma recurrente**.
Si este es el caso, aplicaremos lo del apartado [ACTUALIZAR CLASES WHATSAPP](#actualizar-clases-whatsapp).

2 - En base a lo anterior, teniendo en cuenta que **NO es recurrente** el error de elemento no encontrado, debemos verificar en los email que Sofia envía para chequear en qué proceso hemos tenido error, ya que este no es porque WhatsApp haya cambiado sus clases de los elementos, sino porque la plataforma ha cambiado de lugar un elemento que utiliza Sofía o ha renombrado uno de ellos.
Si es este el caso, debemos verificar la clase o el xPath que tine el elemento que utilizamos en ese proceso para poder actualizar en donde sea necesario.

<hr>

### ACTUALIZAR CLASES WHATSAPP

Para facilitar el proceso de actualización de las mismas se deja una referencia de dónde y qué clase corresponde actualmente a cada elemento que se utiliza desde WhatsApp para poder comprobar si ha cambiado alguna de estas. 

**Estas clases de WhatsApp se encuentran sólo en los archivos <code>wp.py</code> y <code>wpEdge.py</code>**. Se sugiere ver de antemano el código para mayor entendimiento.

De haber cambiado alguna de estas clases seguiremos con el proceso que explicaremos más adelante. 

#### A continuación el nombre de la función y que elemento llama:

**Dentro de <code>mani.py</code>:**

- Función <code>buscar_chats()</code>, variable <code>chats</code> tenemos la clase definida en <code>(By.CLASS_NAME, "_8nE1Y")</code> que equivale al elemento que vemos en la imagen, el cual es la "caja" en donde se encuentra el ultimo chat:

<img width="297" alt="Screenshot 2023-06-20 at 17 19 28" src="https://github.com/not32code232/sofia/assets/134972894/45e609c8-01f4-4cfb-8efe-e6f9e0dff0ea"><br>

- Función <code>buscar_chats()</code>, variable <code>chats_nuevos</code> tenemos la clase definida en <code>(By.CLASS_NAME, "_21S-L")</code> que equivale al elemento que vemos en la imagen, el cual hace referencia a si existe un chat nuevo:

<img width="119" alt="Screenshot 2023-06-20 at 16 26 57" src="https://github.com/not32code232/sofia/assets/134972894/e8d9f2ae-0219-4848-b3c2-d12a0b93fb70"><br>

- Función <code>buscar_chats()</code>, variable <code>chat_numero</code> tenemos la clase definida en <code>(By.CLASS_NAME, "_21S-L")</code> que equivale al elemento que vemos en la imagen, el cual es el numero del cual recibimos el mensaje:

<img width="247" alt="Screenshot 2023-06-20 at 17 26 33" src="https://github.com/not32code232/sofia/assets/134972894/dfc58f63-4777-4c26-b74e-9e608c7c4876"><br>

**Dentro de <code>wp.py</code>:**

- Función <code>leer_ultimo_mensaje()</code>, variable <code>element_box_message</code> tenemos la clase definida en <code>(By.CLASS_NAME, "ItfyB")</code> que equivale al elemento que vemos en la imagen, el cual es la "caja" en donde se encuentra el ultimo mensaje:

<img width="312" alt="Screenshot 2023-06-20 at 17 06 34" src="https://github.com/not32code232/sofia/assets/134972894/3b3fbede-a923-4b67-80db-d50bd6b117c3"><br>

- Función <code>leer_ultimo_mensaje()</code>, variable <code>element_message</code> tenemos la clase definida en <code>(By.CLASS_NAME, "_21Ahp")</code> que equivale al elemento que vemos en la imagen, el cual corresponde al contenido del mensaje:
  
<img width="312" alt="Screenshot 2023-06-20 at 17 08 19" src="https://github.com/not32code232/sofia/assets/134972894/2d960a24-cc4a-4085-b213-611fb55edce2"><br>

- Función <code>buscar_chat()</code>, variable <code>cancel</code> tenemos la clase definida en <code>(By.CLASS_NAME, "-Jnba")</code> que equivale al elemento que vemos en la imagen:
  
<img width="330" alt="Screenshot 2023-06-20 at 16 42 42" src="https://github.com/not32code232/sofia/assets/134972894/2cd94671-0b89-42d2-afeb-a012d82001b7"><br>

Dentro de <code>wpEdge.py</code> se hacen referencia a los mismos elementos **pero NO poseen las mismas clases**, el proceso de verificar es el mismo que <code>wp.py</code> solo que el nombre de las clases sera distinto.

#### Actualizar clase

Este proceso es el mismo para cada uno de los elementos de WhatsApp, en este ejemplo lo haremos con el elemento <code>cancel</code> de la funcion <code>buscar_chat()</code>:

Veamos los pasos:

1. Abierta la ventana de WhatsApp web, ingresamos / abrimos DevTools. 
En el caso de Chrome las DevTools [tutorial aquí](https://developer.chrome.com/docs/devtools/open/) y en el caso de Edge [tutorial aqui](https://learn.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/overview).

3. Hacemos click en el icono de flecha que vemos en la imagen:

<img width="387" alt="Screenshot 2023-06-20 at 17 55 32" src="https://github.com/not32code232/sofia/assets/134972894/aa8ef43c-6bbf-4d18-92fe-12ce83ac8750"><br>

4. Buscamos el elemento que queremos actualizar teniendo en cuenta la guía anterior.

<img width="161" alt="Screenshot 2023-06-20 at 18 01 57" src="https://github.com/not32code232/sofia/assets/134972894/18244223-b7e2-46af-9a3b-e1e3d06e0af8"><br>

5. Encontrado el elemento debemos ver que clase posee el mismo.

<img width="387" alt="Screenshot 2023-06-20 at 18 01 43" src="https://github.com/not32code232/sofia/assets/134972894/7a0f25ed-0b05-48a6-84a3-b0fa6d29b1a7"><br>

6. Con la clase que tiene este elemento ahora, debemos copiar ese valor de clase y pegarlo en nuestro código actualizado.

7. Verificar que esta actualización haya sido correcta corriendo el software nuevamente. De ser correcta la actualización de estas clases, no habrán problemas, de lo contrario seguirá fallando por motivo de que no actualizamos correctamente la clase.

<hr>

### PROCESO LEVANTAR Y CORRER PROYECTO

**Requerimientos previos para iniciar:**

1. Servidor VPS con un mínimo de 16 GB de RAM con sistema operativo Windows Server 2022.
2. Tener el código fuente del proyecto listo para importar o descargar.

**Paso a paso:**

1. Instalar en la máquina la última versión de Python (https://www.python.org/downloads/).

2. Abrimos la terminal de nuestro equipo y en la carpeta raíz correremos el siguiente comando para instalar las dependencias necesarias: <code>pip install selenium pandas numpy mysql-connector-python unidecode pyautogui</code>.

3. Descomprimimos nuestra carpeta del proyecto dejándola disponible en escritorio para facilitar el acceso.

4. Configuramos datos iniciales:

Para poder iniciar el proyecto correctamente, previamente necesitamos de ciertos datos iniciales los cuales agregaremos en el archivo que se encuentra dentro del proyecto con el nombre <code>config.py</code> donde veremos lo siguiente y completaremos con nuestros datos aquello que se nos pide en este archivo:

- num administrador 
- num superadministrador
- usuario y contrasena panel plataforma
- nombre de bot
- datos de transferencia
- url de la plataforma
- cbu de cuenta a transferir
- alias de cuenta a transferir
- nombre de cuenta a transferir
- user config (solo gama planeta, este nombre de usuario debe comenzar con A)

  **SCREENSHOT DE UN COFIG LISTO**

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

15. Para que el bot de avisos a los canales, deberemos crearlos de forma manual, en este canal debe ser miembro el numero que se posee el bot y el administrador.
    
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

**CASO PULPOBET:**

16. Abrimos una nueva consola (terminal) ubicándonos nuevamente en la raíz del proyecto y corremos el archivo <code>main.py</code> con el comando <code>python supermain.py</code>. Con este se nos abrirá una ventana con la plataforma donde deberemos realizar lo siguiente:

- En la parte superior donde vemos las páginas, seleccionar modo vista con la mayor cantidad disponible, ejemplo 50.
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- Dejamos en primer plano esta ventana en pantalla completa.
- Controlamos de tener habilitado el "Incluir Bloqueados".

Quedandonos con una vista de la siguiente forma:

<img width="500" alt="Screenshot 2023-06-06 at 10 58 21" src="https://github.com/not32code232/sofia/assets/134972894/9acd94a5-fb1d-46c7-a7fd-f8185af1b911"><br>

**CASO GAMA PLANETA:**

**CHECKEAR SI ESTE PASO LO AUTOMATIZAMOS** - Todos los paneles de la gama de planeta, debe que existir un usuario que empiece con la letra A (para que este al principio) y tiene que cargarse al config.py en la variable user_config.
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- **IMPORTANTE**, en esta gama NO debe haber agentes en el panel, solo debe haber jugadores,si este tiene agentes puede no funcionar.

**GAMA JUGALO:**
- Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
- Seleccionar si no lo esta, el boton "Todos" en el area de la tabla de usuarios.

17. ¡Listo para trabajar! Ahora solo queda hacer unas breves pruebas para comprobar que todo esté correctamente funcionando y ya podemos dejarlo corriendo. De lo contrario deberemos volver a los pasos o identificar el error para hacerlo que funcione.
