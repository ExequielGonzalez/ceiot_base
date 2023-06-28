# Ejercicio CiberKillChain - Defensa


## Alumno

Exequiel Gonzalez

## Enunciado

Desarrollar la defensa en función del ataque planteado en orden inverso. No es una respuesta a un incidente, hay que detectar el ataque independientemente de la etapa.

Para cada etapa elegir una sola defensa, la más importante, considerar recursos limitados.

## Resolución

### Ataque realizado:

El atacante ingresó en una oficina a la cual no tenía acceso y sustrajo información valiosa de la empesa.

### Cyberkillchain al inverso para definir mitigaciones posibles

### 7. Actions on Objectives.

El equipo de seguridad de la empresa junto con la policia recaban información de lo sucedido. La gente de sistemas comprueba que el sistema de acceso solamente registró ingresos y egresos con credenciales validas, por lo tanto se supone que estas fueron vulneradas.

Una acción importante para mitigar sucesos similares a este en el futuro es realizar copias de seguridad periódicas de los datos sensibles y almacenar las copias en ubicaciones seguras y separadas, para mitigar el impacto de la pérdida o sustracción de información.
-   [M1053 - Data Backup](https://attack.mitre.org/mitigations/M1053/)


Además y no menos importante, se debe implementar cifrado de datos para proteger la información almacenada localmente en la oficina de forma de mitigar las posibles perdidas.

-   [M1041 - Encrypt Sensitive Information](https://attack.mitre.org/mitigations/M1041/)

### 6. Command & Control

Desconociendo la forma en que fue vulnerado el sistema, en esta etapa el razonamiento lógico es analizar el trafico de red en busca anomalias:

[DS0029 - Network Traffic](https://attack.mitre.org/datasources/DS0029/)

En caso de encontrar algo sospechoso, se deberían tener alertas que permitan detener a tiempo un posible ataque. Mitigación.

[M1031 - Network Intrusion Prevention](https://attack.mitre.org/mitigations/M1031/)

### 5. Installation

Si se cree que el sistema esta comprometido, una primera medida de mitigación en esta etapa sería la de bloquear todo código que se ejecute en el sistema de control de accesso.

[M1038 - Execution Prevention](https://attack.mitre.org/mitigations/M1038/)

  
### 4. Exploit

Aquí se deben impedir ingresos no autorizados al sistema. Hay dos medidas muy importantes para aplicar que pueden tener un impacto muy positivo en la seguridad del sistema:

[M1026 - Privileged Account Management](https://attack.mitre.org/mitigations/M1026/)

[M1032 - Multi-factor Authentication](https://attack.mitre.org/mitigations/M1032/)

En primer lugar, se deben revisar los permisos del sistema, y asignar permisos de acceso a las personas que realmente lo necesitan. Luego, es muy importante utilizar un sistema de multi-factor para la autenticación, ya que reduce notablemente la probabilidad de ingresos no deseados.

Implementar un ingreso multifactor puede ser costoso en este sistema, por eso se proponen dos medidas de mitigación.


### 3. Delivery

Para mitigar esta etapa, el primer control que se puede realizar es el de limitar y controlar el nuevo hardware que se instala en la fabrica, ya que uno de estos podría estar actuando con sniffer de la red LoRa.

[M1034 - Limit Hardware Installation](https://attack.mitre.org/mitigations/M1034/)

  Una forma de ayudar al control de lo anterior, es a través del entrenamiento de los empleados de la empresa, de forma que estos puedan identificar hardware sospechoso en su perimetro de trabajo. Esto último podría ser muy costoso y poco efectivo dada la forma de delivery utilizada en el ataque.

[M1017 - User Training](https://attack.mitre.org/mitigations/M1017/)



### 2. Weaponization

Se considera que no hay forma de impedir que un atacante pueda adquirir el hardware necesario para realizar un ataque.


### 1. Reconnaissance

Si bien es posible buscar en internet información sobre los empleados con alto privilegio, esto no implica encontrar algún dato que deba ser considerado como vulnerable.

Si sería efectivo buscar información en la red sobre el sistema de acceso para conocer si existe alguna vulnerabilidad conocida.

[DS0035 - Internet Scan](https://attack.mitre.org/datasources/DS0035/)

