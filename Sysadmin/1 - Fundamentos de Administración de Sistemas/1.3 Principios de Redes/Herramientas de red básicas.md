
#### Introducción

En el mundo de la administración de sistemas y redes, Linux ofrece un conjunto robusto de herramientas de línea de comandos que son esenciales para la gestión y resolución de problemas en redes. Estas herramientas permiten a los administradores monitorizar, analizar y configurar aspectos cruciales de la red. A continuación, se presentan algunas de las herramientas básicas más importantes para redes en Linux.

---

### ifconfig y ip

**ifconfig**:
- **Definición**: `ifconfig` (interface configuration) es una herramienta tradicional utilizada para configurar interfaces de red en sistemas Unix-like.
- **Uso Básico**:
  - Mostrar la configuración de las interfaces de red: `ifconfig`.
  - Asignar una dirección IP a una interfaz: `ifconfig eth0 192.168.1.10 netmask 255.255.255.0`.
  - Activar o desactivar una interfaz de red: `ifconfig eth0 up` / `ifconfig eth0 down`.

**ip**:
- **Definición**: `ip` es una herramienta más moderna y versátil que reemplaza a `ifconfig` para la configuración de interfaces de red y administración de rutas.
- **Uso Básico**:
  - Mostrar información de todas las interfaces: `ip addr show`.
  - Asignar una dirección IP a una interfaz: `ip addr add 192.168.1.10/24 dev eth0`.
  - Activar o desactivar una interfaz de red: `ip link set eth0 up` / `ip link set eth0 down`.

---

### ping

**Definición**:
- `ping` es una herramienta básica utilizada para verificar la conectividad entre dos dispositivos de red.

**Uso Básico**:
- Verificar la conectividad con una dirección IP o nombre de dominio: `ping 192.168.1.1` o `ping www.example.com`.
- Enviar un número específico de paquetes: `ping -c 4 192.168.1.1`.

**Funcionamiento**:
- `ping` envía paquetes ICMP Echo Request al destino y espera respuestas ICMP Echo Reply, proporcionando información sobre la latencia y la pérdida de paquetes.

---

### traceroute

**Definición**:
- `traceroute` es una herramienta utilizada para rastrear la ruta que toman los paquetes desde el origen hasta el destino.

**Uso Básico**:
- Rastrear la ruta a un destino: `traceroute www.example.com`.

**Funcionamiento**:
- `traceroute` envía paquetes con TTL (Time To Live) incrementando y muestra la dirección IP de cada enrutador intermedio hasta alcanzar el destino final, proporcionando información sobre los tiempos de tránsito.

---

### netstat y ss

**netstat**:
- **Definición**: `netstat` (network statistics) es una herramienta utilizada para mostrar estadísticas de red, conexiones y puertos abiertos.
- **Uso Básico**:
  - Mostrar todas las conexiones de red: `netstat -a`.
  - Mostrar estadísticas de las interfaces de red: `netstat -i`.

**ss**:
- **Definición**: `ss` (socket statistics) es una herramienta más moderna que reemplaza a `netstat` para la visualización de información de sockets.
- **Uso Básico**:
  - Mostrar todas las conexiones TCP: `ss -t -a`.
  - Mostrar estadísticas de las interfaces de red: `ss -i`.

---

### dig y nslookup

**dig**:
- **Definición**: `dig` (Domain Information Groper) es una herramienta para consultar servidores DNS.
- **Uso Básico**:
  - Consultar un registro A para un dominio: `dig example.com`.
  - Consultar un servidor DNS específico: `dig @8.8.8.8 example.com`.

**nslookup**:
- **Definición**: `nslookup` es otra herramienta para consultar servidores DNS, aunque más simple y con menos opciones que `dig`.
- **Uso Básico**:
  - Consultar un dominio: `nslookup example.com`.
  - Consultar un servidor DNS específico: `nslookup example.com 8.8.8.8`.

---

### tcpdump

**Definición**:
- `tcpdump` es una herramienta de análisis de tráfico de red que permite capturar y visualizar los paquetes que pasan por una interfaz de red.

**Uso Básico**:
- Capturar y mostrar tráfico en una interfaz: `tcpdump -i eth0`.
- Guardar la captura en un archivo: `tcpdump -i eth0 -w captura.pcap`.

**Filtros**:
- Filtrar tráfico por protocolo: `tcpdump -i eth0 tcp`.
- Filtrar tráfico por dirección IP: `tcpdump -i eth0 host 192.168.1.1`.

---

### nmap

**Definición**:
- `nmap` (Network Mapper) es una herramienta utilizada para el escaneo de redes y la auditoría de seguridad.

**Uso Básico**:
- Escanear los puertos abiertos en una dirección IP: `nmap 192.168.1.1`.
- Escanear una red completa: `nmap 192.168.1.0/24`.

**Opciones Avanzadas**:
- Escaneo de puertos específicos: `nmap -p 22,80,443 192.168.1.1`.
- Detección de sistema operativo: `nmap -O 192.168.1.1`.
