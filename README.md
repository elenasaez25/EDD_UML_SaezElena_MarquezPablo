## INTRODUCCIÓN

Este trabajo consiste en realizar un diagrama de actividad del modelado de un proceso de compra, en concreto la confirmación de un pedido. Antes de crear dicho diagrama, es necesario realizar una investigación sobre la sintaxis de UML 2.5 e información sobre la realización de pedidos. Además de estos dos pasos, luego hay que justificar nuestro diagrama y complementarlo con una bibliografía en estilo IEEE.

## INVESTIGACIÓN PREVIA 

1. Sintaxis específica de UML 2.5 para nodos de control [\[1\]](https://www.viz-tools.com/es/uml-activity-diagram-symbols-notations-guide/) [\[2\]](https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/diagramas-de-actividades-uml/)

- **Nodo inicial:** Circulo negro que marca el inicio   
- **Nodo final:** Circulo negro rodeado por un anillo que indica el final de la actividad.  
- **Nodo de decisión:** Un rombo que dirige el flujo hacia una salida mediante una condición por corchetes.   
- **Nodo de fusión:** Recibe múltiples flujos de entrada y emite un único flujo de salida  
- **Nodos de bifurcación (barra de fork):** Representado por una barra gruesa horizontal que divide un flujo entrante en varias salidas simultáneas.  
- **Nodos de sincronización (Join):** Representado por una barra gruesa horizontal que, en diferencia de la barra de de fork, espera la llegada de todos los flujos entrantes antes de permitir la salida.  
- **Flujos de control:** Se representan mediante flechas con punta abierta que conectan los nodos  
- **Flujos de objetos:** Se representan mediante líneas punteadas con flechas, indican el movimiento de los datos entre los nodos de acción

2. Diferencia entre una decisión (rombo) y una bifurcación (barra de fork)  [\[3\]](https://es.wikipedia.org/wiki/Bifurcaci%C3%B3n_\(sistema_operativo\))

   **La decisión** permite al flujo tomar distintos caminos basados en una condición lógica de Sí o No.  
   El funcionamiento del flujo es que entra por un lado y sale por dos lados posibles (o más, dependiendo del caso) y **determina la instrucción que se va a ejecutar después.** Su funcionamiento es cambiar el flujo de instrucciones.  
     
   En cambio, **la bifurcación** crea una copia idéntica del proceso actual generando un “proceso hijo” que **sigue su propia ejecución independientemente del “proceso padre”**. Su funcionamiento es aislar cambios o duplicar la ejecución del sistema.  
     
     
     
   

## MODELADO DEL PROCESO DE COMPRA

Para representar la confirmación de un pedido de una tienda online, es necesario tener en cuenta los siguientes pasos:

1. El flujo empieza cuando el usuario pulsa “Finalizar compra”.  
2. Luego, el sistema debe validar a la vez el Stock y dicha sesión.  
3. Si las dos restricciones anteriores son correctas, toca realizar el pago.  
4. Si el pago es exitoso, el sistema debe ejecutar de forma paralela las siguientes acciones:  
   1. Registro del pedido en la base de datos.  
   2. Generación del PDF de la factura.  
   3. Envío de notificación por correo electrónico.  
5. Finalmente, cuando todas las acciones anteriores han sido completadas, se muestra un mensaje de confirmación al cliente.

## BIBLIOGRAFÍA

