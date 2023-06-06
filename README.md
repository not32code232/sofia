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

<hr>
