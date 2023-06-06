### SOFIA BOT DOC

<hr>

### SOLUCION

Automarizar el proceso que se realiza entre el jugador, cajero y plataforma acelerando los tiempos de respuesta y eliminando la interaccion por parte del cajero al máximo nivel.

<hr>

### INDICE

- [FLUJO COMPLETO](#flujo-completo)
- [STACK TECNOLOGICO](#stack-tecnologico)
- [COMANDOS ADMINISTRADOR](#comandos-administrador)
- [IDENTIFICAR ERRORES Y REPORTE](#identificar-errores-y-reporte)
- [ROL PROPIETARIO](#rol-propietario)
- [ROL ADMINISTRADOR](#rol-administrador)
- [PROCESO LEVANTAR Y CORRER PROYECTO](#proceso-levantar-y-correr-proyecto)

<hr>

### FLUJO COMPLETO

![flujoCompletoSofia](https://github.com/not32code232/sofia/assets/134972894/133b27c3-3733-47f1-805e-9a6fd281e85d)

<hr>

### STACK TECNOLOGICO

El proyecto se construye utilizando las siguientes tecnologías:

- Python
- Selenium
- PyAutoGUI
- XAMPP MySQL
- Pandas
- Numpy

Conociendo las bases de cada una de estas podremos desarrollar, corregir o modificar el mismo con mayor entendimiento. Para este entendimiento se debe tener en cuenta el flujo general.

<hr>

### COMANDOS ADMINISTRADOR

**Aclaraciones de documento**

Las palabras en negrita son palabras clave, por ende SIEMPRE se envían igual al momento de realizar el comando.
Las palabras subrayadas NO siempre se envían igual, esto depende de la ocasión.
Cuando el administrador envíe un comando SIEMPRE espere una respuesta antes de enviar otro.

**Comandos**

- Carga:

Cancelar carga: <code>Carga + número de operación + cancelar</code>

Carga recibida: <code>Carga + número de operación + recibido + monto</code>

- Descarga:

Cancelar descarga: <code>Descarga + número de operación + cancelar</code>

Descarga transferida: <code>Descarga + número de operación + transferido</code>

- Consultar fichas en panel de administrador: <code>Fichas panel</code>

- Cambiar datos bancarios para pasos de transferencia: <code>Banco + cbu + alias + nombre de cuenta</code>

<hr>

### IDENTIFICAR ERRORES Y REPORTE

Este apartado ha sido simplificado de manera que se puedan identificar de manera rápida y efectiva los errores y ver el estado del software accediendo al canal de WhatsApp en el cual Sofía enviará estos reportes.

**Funcionalidad y uso:**

Sofia a medida que va realizando sus acciones, desde leer el chat, hasta cumplir con lo que el jugador o administrador solicitó, cada que ingresa a una nueva funcionalidad va registrando en que proceso / funcionalidad se encuentra. Si en el mismo proceso ha sucedido algún tipo de error, se registra este y se devuelve en el canal de WhatsApp con el detalle de cuál fue el último proceso que se realizó para poder ubicarlo dentro del código y realizar correcciones de ser necesarias.

Si deseamos corregir algún error o simplemente acceder al código para verificar su funcionamiento o causa del error, debemos abrir nuestro proyecto en el editor de preferencia y buscar en el proyecto el nombre de la función que ha generado ese error, el cual nos llevara a donde se encuentra toda la lógica de ese proceso y verificar o corregir lo que debamos.

<hr>

### ROL PROPIETARIO

<hr>

### ROL ADMINISTRADOR

<hr>

### PROCESO LEVANTAR Y CORRER PROYECTO

**Requerimientos previos para iniciar:**

1. Servidor VPS con un mínimo de 16 GB de RAM con sistema operativo Windows Server 2022.
2. Tener el código fuente del proyecto listo para importar o descargar.

**Paso a paso:**

1. Instalar en la máquina la última versión de Python (https://www.python.org/downloads/).

2. Abrimos la terminal de nuestro equipo y en la carpeta raíz correremos el siguiente comando para instalar las dependencias necesarias: <code>pip install selenium pandas numpy mysql-connector-python unidecode pyautogui</code>

3. Agregamos contraseña del panel?

4. Descargamos de la siguiente dirección [Apache Friends](https://www.apachefriends.org/index.html) la última versión de XAMPP para windows, esto nos permitirá tener nuestra base de datos corriendo.

<img width="500" alt="Screenshot 2023-06-05 at 22 40 51" src="https://github.com/not32code232/sofia/assets/134972894/b0a8ae7a-c9f0-4d2f-90ad-6841f7e9a806">

5. Una vez instalado XAMPP lo iniciamos y damos a <code>start</code> a MySQL.

<img width="500" alt="Screenshot 2023-06-05 at 22 41 54" src="https://github.com/not32code232/sofia/assets/134972894/d10e7039-6b20-46af-8782-c33677a508bf">

6. Ingresamos dentro del navegador a la ruta <code>localhost/phpmyadmin</code> en donde nos llevará al panel de administrador de la base de datos PHP, en esta deberemos importar el archivo que se encuentra dentro de la carpeta <code>resource</code> con la extensión de .sql.

7. Descomprimimos nuestra carpeta del proyecto dejándola disponible en escritorio para facilitar el acceso.

8. Descargar e instalar el navegador Microsoft Edge ([Download Microsoft Edge](https://www.microsoft.com/en-us/edge/download)).

<img width="500" alt="Screenshot 2023-06-06 at 08 41 00" src="https://github.com/not32code232/sofia/assets/134972894/5ef2eddd-e636-4969-9ebf-421608e1a0bd">

9. Descargar e instalar el navegador Google Chrome ([Google Chrome - Download the Fast, Secure Browser from Google](https://www.google.com/chrome/)).

10. Descargar Web Driver para Edge validando la versión y descargando el correspondiente a la misma, instructivo a detalle en página oficial: [Edge Webdriver](https://learn.microsoft.com/en-us/microsoft-edge/webdriver-chromium/?tabs=c-sharp#download-microsoft-edge-webdriver).

11. Descargar Web Driver para Chrome validando la versión y descargando el correspondiente a la misma en [ChromeDriver](https://chromedriver.chromium.org/downloads), descargando la versión de windows disponible. Es importante validar su versión en ambos navegadores, esta información la veremos en detalles del navegador.

<img width="500" alt="Screenshot 2023-06-06 at 08 43 06" src="https://github.com/not32code232/sofia/assets/134972894/44aab0f6-33b6-4fc2-ac00-bc078172f4f9"><br>

<img width="500" alt="Screenshot 2023-06-06 at 08 43 55" src="https://github.com/not32code232/sofia/assets/134972894/bdfb25bd-dcc1-4798-afe6-2f3a5a1f96dc">

12. Una vez descargados los drivers los ubicamos a ambos en la carpeta <code>driver</code> del proyecto, cada uno con su nombre <code>chromedriver</code> y <code>edgedriver</code>.

13. Abrir la terminal (cmd) y ubicarnos en la carpeta base donde tenemos el proyecto y correr el archivo <code>KeepSession.py</code> con el comando <code>python KeepSession.py</code>, esperamos a que se nos abra el Chrome y se cargue WhatsApp Web en donde tendremos que escanear para poder ingresar con el número que será el que reciba a los jugadores, administradores y envíe informes. 
Es importante que NO cerremos la consola el cual corrimos ese comando y NO cancelamos el proceso. Una vez ingresado nuestro WhatsApp, dejar así tal cual sin tocar nada más ni ingresar a ningún chat.

14. Repetimos el paso anterior solo que en vez de con el archivo <code>KeepSession.py</code>, será con el archivo <code>KeepSessionEdge.py</code> corriendo el comando <code>python KeepSessionEdge.py</code>. 

<i>Es importante que NO cerremos la consola el cual corrimos ese comando y NO cancelamos el proceso.</i>

**CASO PULPOBET:**

15. Abrimos una nueva consola (terminal) ubicándonos nuevamente en la raíz del proyecto y corremos el archivo <code>main.py</code> con el comando <code>python main.py</code>. Con este se nos abrirá una ventana con la plataforma donde deberemos realizar lo siguiente:
a. Habilitar vista de bloqueados.
b. En la parte superior donde vemos las páginas, seleccionar modo vista con la mayor cantidad disponible, ejemplo 50.
c. Con las teclas Ctrl + Menos (-) quitaremos zoom hasta el nivel 33% o cercano.
d. Dejamos en primer plano esta ventana en pantalla completa.

16. ¡Listo para trabajar! Ahora solo queda hacer unas breves pruebas para comprobar que todo esté correctamente funcionando y ya podemos dejarlo corriendo. De lo contrario deberemos volver a los pasos o identificar el error para hacerlo que funcione.

<hr>
