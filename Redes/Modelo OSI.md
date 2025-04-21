### ¿Porqué el modelo OSI esta dividido en capas?
para mostrar visualmente y descriptivamente, lo que puede pasar en los intercambios de datos de dos sistemas comunicados en red.
1. Capa Física: los elementos fisicos relacionada con los dispositivos conectados a una red. 
2. Capa del Enlace de Datos: esta capa es la que hace la transferencia de datos entre dos sistemas cableados o en red. Hace que los datos se transmitan
	1. SubCapa LLC (Control de Enlace Lógico): convertir las señales en unos y ceros
	2. MAC(Control de acceso al medio): se encarga de mover los paquetes de datos de 1 y 0 de un dispositivo a otro.
3. Capa de Red: lleva a cabo el enrutamiento (por los ruters o otros tipos de ruters). 
	1. Protocolo OSPF: es el protocolo que se encarga de llevar las redes por el sitio mas rápido posible.
	2. IP: Las direcciones IP forman parte de esta capa, sirven para identificar los dispositivos de los cuales que se quiere transmitir información, se miran los extremos.
	3. IPSec
	4. ARP
	5. NAT
	6. ICMP
4. Capa de transporte: aquí se encuentran los protocolos TCP y UDP, esta capa se encarga de controlar la transmisión de datos a través de estos protocolos, uno de ellos se encarga de verificar la integridad de la información automáticamente (), y la otra no (UDP). Se coordina el transito e intercambio de datos
5. Capa de Sesión: 
	1. Protocolo NetBIOS 
	2. Protocolo RPC
	3. Protocolo PPTP
	4. Protocolo PAP
6. Capa de presentación: esta capa se encarga por ejemplo del cifrado y descifrado de los datos. Se encarga de darle un formato para poder ver los datos en la capa siguiente.
7. Capa de aplicación: 
	1. HTTPs
	2. DNS
	3. FTP
	4. SMTP