# Actvidad-Refuerzo

## Integrantes
Samuel Espitia  
Miguel Ángel Feo  
Carlos Zuluaga

# Tipo de red seleccionado 



La solución implementada se basa en conectividad Wi-Fi, dado que es una tecnología ampliamente disponible en el campus universitario, con cobertura suficiente para enlazar los distintos sensores distribuidos por puntos estratégicos. 

# Protocolos de Comunicación 

Se empleó el protocolo MQTT (Message Queuing Telemetry Transport) por sus ventajas en entornos IoT: bajo consumo de ancho de banda, eficiencia energética y facilidad de implementación. Este protocolo sigue un modelo de publicación/suscripción ideal para transmitir datos de sensores a una plataforma de monitoreo centralizada. 
En el caso del sistema IoT para el monitoreo de agua y cloro, los sensores encargados de monitorear cada una de las variables actúa como un "publicador". Los sensores envían los datos de cantidad de agua consumida y niveles de cloro a un "broker" MQTT. 
El broker MQTT es ejecutado en un microcontrolador, el cual será el intermediario que se encarga de recibir los datos enviados por los sensores y distribuirlos a los suscriptores correspondientes, en este caso, una plataforma de monitoreo que visualiza estos datos en tiempo real. 

# Descripción del diseño  

El proyecto establecido en este caso busca demostrar la medición de consumo del agua, utilizando un monitor de cantidad de agua, y un componente el cual permite simular el uso del agua ya sea de un lavamanos, una manguera, entre otros.  
