
### Configuración Básica de Red en Linux

#### Utilizando `ifconfig` y `ip`

**Configuración de Dirección IP con `ifconfig`**:
- **Mostrar la configuración de la red**:
  ```bash
  ifconfig
  ```
- **Asignar una dirección IP a una interfaz**:
  ```bash
  sudo ifconfig eth0 192.168.1.10 netmask 255.255.255.0
  ```
- **Activar una interfaz de red**:
  ```bash
  sudo ifconfig eth0 up
  ```
- **Desactivar una interfaz de red**:
  ```bash
  sudo ifconfig eth0 down
  ```

**Configuración de Dirección IP con `ip`**:
- **Mostrar la configuración de la red**:
  ```bash
  ip addr show
  ```
- **Asignar una dirección IP a una interfaz**:
  ```bash
  sudo ip addr add 192.168.1.10/24 dev eth0
  ```
- **Activar una interfaz de red**:
  ```bash
  sudo ip link set eth0 up
  ```
- **Desactivar una interfaz de red**:
  ```bash
  sudo ip link set eth0 down
  ```

#### Configuración de Rutas

**Agregar una ruta estática**:
- Con `route`:
  ```bash
  sudo route add default gw 192.168.1.1
  ```
- Con `ip route`:
  ```bash
  sudo ip route add default via 192.168.1.1
  ```

#### Configuración de DNS

**Editar el archivo de configuración de resolv.conf**:
- Añadir servidores DNS:
  ```bash
  sudo nano /etc/resolv.conf
  ```
  ```bash
  nameserver 8.8.8.8
  nameserver 8.8.4.4
  ```

#### Utilizando `netplan` (en sistemas basados en Ubuntu 18.04 y posteriores)

**Archivo de configuración**:
- **Editar configuración de red**:
  ```bash
  sudo nano /etc/netplan/01-netcfg.yaml
  ```
  - Ejemplo de configuración:
    ```yaml
    network:
      version: 2
      ethernets:
        eth0:
          addresses:
            - 192.168.1.10/24
          gateway4: 192.168.1.1
          nameservers:
            addresses:
              - 8.8.8.8
              - 8.8.4.4
    ```
- **Aplicar configuración**:
  ```bash
  sudo netplan apply
  ```

---

### Configuración Básica de Red en Windows

#### Utilizando la Interfaz Gráfica (GUI)

**Configuración de Dirección IP**:
1. **Abrir el Panel de Control**:
   - Ir a `Panel de control` > `Redes e Internet` > `Centro de redes y recursos compartidos`.
2. **Cambiar la configuración del adaptador**:
   - Hacer clic en `Cambiar configuración del adaptador`.
3. **Propiedades de la conexión de red**:
   - Hacer clic derecho en la conexión de red deseada y seleccionar `Propiedades`.
4. **Configuración del Protocolo de Internet versión 4 (TCP/IPv4)**:
   - Seleccionar `Protocolo de Internet versión 4 (TCP/IPv4)` y hacer clic en `Propiedades`.
5. **Asignar dirección IP manualmente**:
   - Seleccionar `Usar la siguiente dirección IP` e ingresar la dirección IP, máscara de subred y puerta de enlace predeterminada.
   - Ingresar los servidores DNS en `Usar las siguientes direcciones de servidor DNS`.

#### Utilizando la Línea de Comandos (CMD)

**Configuración de Dirección IP con `netsh`**:
- **Mostrar configuración de red**:
  ```cmd
  netsh interface ip show config
  ```
- **Asignar una dirección IP**:
  ```cmd
  netsh interface ip set address "Ethernet" static 192.168.1.10 255.255.255.0 192.168.1.1
  ```
- **Configurar servidores DNS**:
  ```cmd
  netsh interface ip set dns "Ethernet" static 8.8.8.8 primary
  netsh interface ip add dns "Ethernet" 8.8.4.4 index=2
  ```

#### Utilizando PowerShell

**Configuración de Dirección IP**:
- **Mostrar la configuración de red**:
  ```powershell
  Get-NetIPConfiguration
  ```
- **Asignar una dirección IP**:
  ```powershell
  New-NetIPAddress -InterfaceAlias "Ethernet" -IPAddress 192.168.1.10 -PrefixLength 24 -DefaultGateway 192.168.1.1
  ```
- **Configurar servidores DNS**:
  ```powershell
  Set-DnsClientServerAddress -InterfaceAlias "Ethernet" -ServerAddresses ("8.8.8.8", "8.8.4.4")
  ```
