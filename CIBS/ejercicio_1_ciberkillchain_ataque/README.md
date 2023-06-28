# Ejercicio CiberKillChain - Ataque
## Alumno

Exequiel Gonzalez


## Enunciado

Armar una cyberkillchain usando técnicas de la matriz de Att&ck para un escenario relacionado al trabajo práctico de la carrera.

## Datos del trabajo práctico

Se tiene un sistema que permite un control de acceso apto para grandes 
superficies en las que es muy costoso o imposible utilizar soluciones tradicionales como las que 
dependen de ethernet o wifi.
Si bien en muchos casos los sistemas de control de acceso son económicos y se encuentran 
muy difundidos, muchos dependen de una infraestructura preexistente que es típica de las 
ciudades. Sin embargo, en determinados casos como barrios residenciales alejados de la 
ciudad, o grandes naves industriales, resulta muy dificultoso trasladar los cables de 
comunicación necesarios a cada uno de los puntos de acceso. Es por esto por lo que se 
propone un nuevo sistema que utilice como medio de comunicación entre los distintos puntos 
la tecnología Wireless LoRa.

El sistema se utilizará para el ingreso y egreso a distintas partes de una fabrica.

Un detalle no menor es que todavía no empecé el trabajo práctico, por lo tanto hay detalles de la implementación no definidos.

-   [Más detalles](https://drive.google.com/file/d/1Hrwj39pJGyVZcCzS1ukyjpUAYAJFTGP2/view) 

## Objetivo del ataque

El objetivo es utilizar vulnerar un sistema como el anterior que se encuentra instalado en una fabrica, de forma de poder ingresar en la oficina de uno de los altos mandos y sustraer información se sabe que solo guarda localmente.

Para esto, se planea analizar el tráfico de datos de la red LoRa para intentar hacerse pasar por una de las personas autorizadas en el sistema de control de acceso.

Se tiene como dato imporante que cada uno de los puntos de acceso envia su información a ser verificada en un servidor utilizando tecnología LoRa.

###  Cyberkillchain


1. Reconnaissance
>Descripción: El atacante junta información de la organización a la cual quiere hacer un daño. Se arma un grafo de información donde el nodo central es la victima.

Se recopila información sobre el sistema de control de acceso basado en la tecnología LoRa y las personas autorizadas en la empresa.

 Técnicas utilizadas:


-   [T1593](https://attack.mitre.org/techniques/T1593/) - Search Open Websites/Domains: Se investigan perfiles de redes sociales y páginas web de los emplados y personal autorizado para obtener información personal, patrones de comportamiento y posibles credenciales.
Además, se busca información sobre la tecnología LoRa utilizada en el sistema de control de acceso.


2. Weaponization
> Descripción: Definición y diseño del plan para atacar a la orgnización. 

Se preparan los recursos necesarios para realizar un ataque basado en el análisis del tráfico de datos de la red LoRa

Técnicas utilizadas:

-   [T1583](https://attack.mitre.org/techniques/T1583/)  -  Acquire Infrastructure Se adquieren dispositivos capaces de interferir con las comunicaciones LoRa para interrumpir el flujo normal de datos y capturar paquetes de información.



3. Delivery
> Descripción: Se pone en marcha el inicio del plan. Se envia los recursos necesario para comenzar con el ataque.

Se lleva a cabo el despliegue de dispositivos de interferencia y sniffing en el área de la oficina objetivo para capturar el tráfico de datos LoRa.

-   [T1040](https://attack.mitre.org/techniques/T1040/)   - Sniffing: Se utilizan herramientas de sniffing para capturar y analizar el tráfico de datos LoRa y extraer información relevante.
Se analizan los paquetes de datos capturados y se busca identificar información sensible y credenciales que permitan hacerse pasar por una de las personas autorizadas en el sistema.
  
4. Exploit

>Descripción: El o los recursos iniciales del ataque logran entrar en la organización de forma controlada (sin ser detectados como una potencial amenaza).

Se utiliza la información y credenciales obtenidas para ingresar en el sistema como una persona autorizada.
  
 -   [T1078](https://attack.mitre.org/techniques/T1040/)   -  Valid Accounts: Se utilizan las credenciales obtenidas para autenticarse como una persona autorizada en el sistema de control de acceso LoRa y obtener acceso no autorizado a las áreas restringidas.
 

  5. Installation

>Descripción: Se establece una presencia persistente en el sistema comprometido para mantener el acceso y control continuo.

Dado que el objetivo principal del ataque es ingresar a la oficina del alto mando de la empresa y sustraer cierta información local no es relevante realizar esta etapa.

6. Command & Control

>Descripción: Se establece una comunicación encubierta entre el atacante y el sistema comprometido sin levantar sospechas.

Se configura una comunicación encubierta entre el atacante y el sistema comprometido para mantener el control y recibir instrucciones adicionales sin ser detectado.

- [T1071](https://attack.mitre.org/techniques/T1071/) - Standard Application Layer Protocol: Se utiliza un protocolo de capa de aplicación estándar para establecer la comunicación encubierta y evitar la detección.

7. Actions on Objectives

>Descripción: El atacante lleva a cabo acciones específicas para lograr su objetivo final.

Se accede a la oficina del alto mando utilizando las credenciales obtenidas y sustrae las pertenencias valiosas.

- [T1005](https://attack.mitre.org/techniques/T1005/) - Data from Local System: Se accede a los archivos y datos almacenados localmente en la oficina del alto mando para identificar las pertenencias valiosas.
- [T1564](https://attack.mitre.org/techniques/T1564/001/) - Hide Artifacts: Se ocultan los registros y rastros de actividad comprometedora para evitar ser detectado.
- [T1560](https://attack.mitre.org/techniques/T1560/001/) - Archive Collected Data: Se recopilan y se almacenan los datos y pertenencias sustraídas para su posterior uso o venta.


