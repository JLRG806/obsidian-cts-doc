### 1.2 Sistemas Operativos Básicos

---

#### Navegación Básica y Comandos en la Terminal

**Comandos Básicos**:
- **`ls`**: Lista archivos y directorios.
  - Ejemplo: `ls -l` (lista en formato largo).
- **`cd`**: Cambia de directorio.
  - Ejemplo: `cd /home` (cambia al directorio /home).
- **`pwd`**: Muestra el directorio actual.
- **`mkdir`**: Crea un nuevo directorio.
  - Ejemplo: `mkdir new_folder`.
- **`rmdir`**: Elimina un directorio vacío.
- **`cp`**: Copia archivos o directorios.
  - Ejemplo: `cp file.txt /backup/`.
- **`mv`**: Mueve o renombra archivos o directorios.
  - Ejemplo: `mv oldname.txt newname.txt`.
- **`rm`**: Elimina archivos o directorios.
  - Ejemplo: `rm -r folder` (elimina un directorio y su contenido).

**Ayuda y Manuales**:
- **`man`**: Muestra el manual de un comando.
  - Ejemplo: `man ls`.
- **`--help`**: Proporciona una breve descripción de uso.
  - Ejemplo: `ls --help`.

#### Gestión de Archivos y Directorios

**Comandos de Archivos**:
- **`touch`**: Crea un archivo vacío o actualiza la fecha de modificación.
  - Ejemplo: `touch file.txt`.
- **`cat`**: Muestra el contenido de un archivo.
  - Ejemplo: `cat file.txt`.
- **`nano`** y **`vi`**: Editores de texto en la terminal.
  - Ejemplo: `nano file.txt` o `vi file.txt`.

**Comandos de Directorios**:
- **`ls -l`**: Lista archivos con detalles.
- **`du`**: Muestra el uso de disco por archivos y directorios.
  - Ejemplo: `du -h` (en formato legible).
- **`df`**: Muestra el espacio en disco disponible.
  - Ejemplo: `df -h` (en formato legible).
- **`chmod`**: Cambia los permisos de archivos o directorios.
  - Ejemplo: `chmod 755 script.sh`.
- **`chown`**: Cambia el propietario de archivos o directorios.
  - Ejemplo: `chown user:user file.txt`.

#### Permisos y Propietarios de Archivos

**Permisos**:
- **Tipos de Permisos**: Lectura (r), escritura (w), ejecución (x).
- **Niveles de Permisos**: Usuario (u), grupo (g), otros (o).
- **Ejemplo de Permisos**: `rwxr-xr--` (usuario tiene todos los permisos, grupo puede leer y ejecutar, otros solo pueden leer).

**Comandos**:
- **`chmod`**: Cambia permisos.
  - Ejemplo: `chmod 644 file.txt` (usuario puede leer y escribir, otros solo leer).
- **`chown`**: Cambia propietario.
  - Ejemplo: `chown user:group file.txt`.

#### Procesos y Gestión de Trabajos

**Comandos de Procesos**:
- **`ps`**: Muestra los procesos actuales.
  - Ejemplo: `ps aux` (muestra todos los procesos en detalle).
- **`top`**: Muestra en tiempo real los procesos y el uso del sistema.
- **`htop`**: Herramienta mejorada de `top` (requiere instalación).

**Gestión de Procesos**:
- **`kill`**: Termina un proceso.
  - Ejemplo: `kill 1234` (termina el proceso con PID 1234).
- **`killall`**: Termina todos los procesos con un nombre dado.
  - Ejemplo: `killall firefox`.
- **`nice`** y **`renice`**: Ajusta la prioridad de un proceso.
  - Ejemplo: `nice -n 10 command` (ejecuta un comando con baja prioridad).
  - Ejemplo: `renice 10 1234` (cambia la prioridad del proceso con PID 1234).

#### Instalación y Gestión de Software

**Gestores de Paquetes**:
- **APT (Debian/Ubuntu)**:
  - **`apt-get install`**: Instala un paquete.
    - Ejemplo: `apt-get install nginx`.
  - **`apt-get update`**: Actualiza la lista de paquetes disponibles.
  - **`apt-get upgrade`**: Actualiza todos los paquetes instalados.
- **YUM (CentOS)**:
  - **`yum install`**: Instala un paquete.
    - Ejemplo: `yum install httpd`.
  - **`yum update`**: Actualiza todos los paquetes instalados.
- **DNF (Fedora)**:
  - **`dnf install`**: Instala un paquete.
    - Ejemplo: `dnf install docker`.
  - **`dnf update`**: Actualiza todos los paquetes instalados.

**Comandos**:
- **Instalación**:
  - **APT**: `sudo apt-get install package_name`.
  - **YUM**: `sudo yum install package_name`.
  - **DNF**: `sudo dnf install package_name`.
- **Actualización**:
  - **APT**: `sudo apt-get update && sudo apt-get upgrade`.
  - **YUM**: `sudo yum update`.
  - **DNF**: `sudo dnf update`.
