# Flow3-NodeRed
Este repositorio contiene los archivos correspondientes al Flow 3 del curso de NodeRed.

## Introducción

Este ejercicio permite demostrar el uso de el Dashboard en NodeRed. Este ejercicio consiste en mostrar la fecha en un tablero con ayuda de los nodos node-red-dashboard. Se usarán los siguentes bloques 

- Inject

   > El nodo **inject** inyecta datos al flow ya sea manualmente o por un intervalo
- Debug

   > El nodo **debug** visualiza el proceso en la barra de debug
- Function
 
   > El nodo **function** ejecuta una función de JavaScript en el mensaje que esta siendo recibido 
- Text

   > El nodo **text** mostrará un texto no editable en el Dashboard 

### Material Necesario

Para realizar este ejercicio necesitaras lo siguente

- [Ubuntu 20.04](https://ubuntu.com/download/desktop)
- [NodeJs](https://nodejs.org/en/)
  - [NPM](https://www.npmjs.com/)
  - [NodeRed](https://nodered.org/)
     - Nodos Dashboard
         > Se pueden instalar desde Manage palette en node red, En este caso instalamos **node-red-dashboard**

### Material de referencia

- [Instalación de Virtual Box](https://edu.codigoiot.com/course/view.php?id=810)
  - [Instalación de Ubuntu 20.04](https://edu.codigoiot.com/course/view.php?id=812)
- [Instalación de NodeRed](https://edu.codigoiot.com/course/view.php?id=817)
- [Intoducción a NodeRed](https://edu.codigoiot.com/course/view.php?id=278)

# Instrucciones

## Requisitos previos

1. Tener instalado todo el software listado en el **Material necesario**
2. Arrancar NodeRed escribiendo el comando `node-red` en la terminal
3. Abrir aplicacion de NodeRed en un navegador con la dirección ["http://localhost:1880"](http://localhost:1880/#flow/d0319225ca32761b)

## Instrucciones de ejecución

1. Se arrastra un nodo de **inject** y se configura de la siguente forma
   - msg.payload = timestamp
   - Repeat = interval
   - every 1 second
   
2. Se arrastra un nodo de **function** y se le escribe el siguente código
   - `var date = new Date(msg.payload)`
     `msg.payload = date.toString();`
     `return msg;`
     
3. Se conecta el nodo **inject** y el nodo **function**

4. Se arrastra un nodo de **Text** de la sección de dashboard

5. Se conecta el nodo de **text** con el nodo de **function**

6. Se arrastra un nodo de **Debug**

7. Se conecta el nodo de **debug** con el nodo de **function**

8. Configurar el nodo de **Text**

9. Configurar el Layout del dashboard

10. Se guarda el flow oprimiendo el botón **Deploy**

# Resultados 

El flow debera verse como el flow de la siguiente imagen

![resultados del flow](https://github.com/davidGalaviz/Flow3-NodeRed/blob/main/Captura%20de%20pantalla%20de%202022-08-26%2013-22-18.png)

Entra a [http://localhost:1880/ui](http://localhost:1880/ui/#!/0?socketid=OGWdowKrOPcSz4pfAAAD) para ver el Dashboard

![resultados en el Dashboard](https://github.com/davidGalaviz/Flow3-NodeRed/blob/main/Captura%20de%20pantalla%20de%202022-08-26%2013-34-56.png)

## Evidencias

[Repositorio](https://github.com/davidGalaviz/Flow3-NodeRed)

# Creditos

Desarrollado por David Galaviz

[GitHub](https://github.com/davidGalaviz)

