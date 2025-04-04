# Actvidad-Refuerzo

## Integrantes
Samuel Espitia  
Miguel Ángel Feo  
Carlos Zuluaga

# Tipo de red seleccionado 

La solución implementada se basa en conectividad Wi-Fi, dado que es una tecnología ampliamente disponible en el campus universitario, con cobertura suficiente para enlazar los distintos sensores distribuidos por puntos estratégicos. 

# Protocolos de Comunicación 

Se empleó el protocolo MQTT (Message Queuing Telemetry Transport) por sus ventajas en entornos IoT: bajo consumo de ancho de banda, eficiencia energética y facilidad de implementación. Este protocolo sigue un modelo de publicación/suscripción ideal para transmitir datos de sensores a una plataforma de monitoreo centralizada. [1]
En el caso del sistema IoT para el monitoreo de agua y cloro, los sensores encargados de monitorear cada una de las variables actúa como un "publicador". Los sensores envían los datos de cantidad de agua consumida y niveles de cloro a un "broker" MQTT. [3]
El broker MQTT es ejecutado en un microcontrolador, el cual será el intermediario que se encarga de recibir los datos enviados por los sensores y distribuirlos a los suscriptores correspondientes, en este caso, una plataforma de monitoreo que visualiza estos datos en tiempo real. 

# Descripción del diseño  
Principalmente se establecieron los roles, donde 2 personas se encargaron de buscar la forma en la que se debian trabajar los componentes en el cisco packet tracer, y la otra persona tenia que realizar el diseño con las indicaciones dadas por los otros integrantes

El proyecto establecido en este caso busca demostrar la medición de consumo del agua, utilizando un monitor de cantidad de agua, y un componente el cual permite simular el uso del agua ya sea de un lavamanos, una manguera, entre otros.[2]  
En la imagen se puede ver el diseño planteado, donde se tiene un servidor, un pc el cual va a permitir monitorear los datos obtenidos de los componentes IoT, que en este caso es un monitor del uso del agua, y una regadera que se puede tomar como una forma de uso de agua, que es lo que se buscaba con la actividad.  
![](https://github.com/miguelangelfeo/Actvidad-Refuerzo-/blob/master/imagen_2025-03-28_211237182.png)

En el diseño, en el servidor se dispuso de una red IP, la cual aloja un servidor web, el cual permite ver y controlar los componentes IoT, en el pc se puede ver esta información, se puede activar el componente que simula el gasto del agua, e instantáneamente se comienza a aumentar la cantidad de agua utilizada, y esto se muestra en el monitor de agua. Además, se tiene el MCU el cual permite encender un led definiendo un límite utilizando los datos recolectados con los sensores.  
 
# Validación de Diseño 

Las pruebas realizadas en el proyecto consistieron en verificar la conectividad y la transmisión de datos entre los sensores y la plataforma de monitoreo a través del protocolo MQTT. En el caso de la simulación, la conexión debía evidenciarse mediante la visualización del de los niveles de agua en el monitor y el funcionamiento de un actuador, el LED. El diseño fue capaz de pasar estas pruebas, mostrando una correcta conexión entre los componentes.  

Al principio se encontraron desafíos debido a la falta de conocimiento de cómo aplicar MQTT en packet tracer, y la manera en la que los dispositivos se podrían conectar. Pero finalmente se logró encontrar una solución mediante investigaciones y se logró comprender correctamente el funcionamiento de estos

# Referencias
[1] “¿Qué es el MQTT? - Explicación del protocolo MQTT - AWS”. Amazon Web Services, Inc. Accedido el 29 de marzo de 2025. [En línea]. Disponible: https://aws.amazon.com/es/what-is/mqtt/

[2] Fernando Méndez. Cisco Packet Tracer - Sensor de Agua | Water Sensor | LCD | MCU. (9 de julio de 2019). Accedido el 29 de marzo de 2025. [Video en línea]. Disponible: https://www.youtube.com/watch?v=LCqogQk_DMg

[3] RKiLAB. Setting UP MQQT Broker and Client In Cisco Packet Tracer. (14 de abril de 2023). Accedido el 29 de marzo de 2025. [Video en línea]. Disponible: https://www.youtube.com/watch?v=AY4TiM2uldI
