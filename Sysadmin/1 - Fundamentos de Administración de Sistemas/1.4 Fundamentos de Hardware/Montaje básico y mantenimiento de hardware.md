
#### Introducción

El montaje y mantenimiento del hardware es una habilidad esencial para los administradores de sistemas. Asegura que los servidores funcionen de manera óptima y reduce el tiempo de inactividad debido a fallos de hardware. En esta sección, se describen los pasos básicos para montar un servidor y las prácticas recomendadas para su mantenimiento.

---

### Montaje Básico de Hardware

#### Preparación

**1. Planificación**:
- **Requisitos del Sistema**: Determinar los requisitos de hardware basados en la carga de trabajo, aplicaciones y usuarios.
- **Espacio y Ubicación**: Seleccionar un espacio adecuado en el centro de datos con suficiente ventilación y acceso a energía y redes.

**2. Herramientas Necesarias**:
- Destornilladores (Phillips y planos).
- Correas antiestáticas.
- Organizador de cables.
- Manuales de instalación de hardware.

#### Montaje de un Servidor

**1. Instalación de la Placa Base**:
- **Montaje**: Colocar la placa base en la carcasa del servidor alineando los agujeros con los separadores y atornillarla firmemente.
- **Conexiones**: Conectar los cables de alimentación de la placa base y los conectores del panel frontal (interruptores y LEDs).

**2. Instalación del Procesador (CPU)**:
- **Colocación**: Abrir el socket de la CPU en la placa base, colocar el procesador cuidadosamente alineando los pines y cerrar el socket.
- **Refrigeración**: Aplicar pasta térmica en la superficie de la CPU y montar el disipador de calor o el sistema de refrigeración líquida según las instrucciones del fabricante.

**3. Instalación de la Memoria (RAM)**:
- **Ranuras**: Identificar las ranuras de RAM en la placa base y abrir los pestillos de las ranuras.
- **Inserción**: Insertar los módulos de RAM alineándolos correctamente y presionar hasta que los pestillos los aseguren en su lugar.

**4. Instalación de Dispositivos de Almacenamiento**:
- **Montaje de Discos**: Montar los HDD o SSD en las bahías correspondientes de la carcasa del servidor.
- **Conexiones**: Conectar los cables de datos (SATA, NVMe) y alimentación a los discos.

**5. Instalación de Tarjetas de Expansión**:
- **Ranuras PCIe**: Identificar las ranuras PCIe en la placa base y retirar las cubiertas de las ranuras de expansión de la carcasa.
- **Inserción**: Insertar las tarjetas (como NIC, controladores RAID) en las ranuras PCIe y asegurarlas con tornillos.

**6. Conexión de la Fuente de Alimentación (PSU)**:
- **Montaje de la PSU**: Montar la PSU en la carcasa del servidor y asegurarla con tornillos.
- **Cableado**: Conectar los cables de alimentación a la placa base, CPU, discos y otros componentes según sea necesario.

**7. Organización de Cables**:
- **Gestión de Cables**: Utilizar bridas y organizadores de cables para mantener el interior de la carcasa ordenado y mejorar el flujo de aire.

---

### Mantenimiento de Hardware

#### Mantenimiento Preventivo

**1. Limpieza Regular**:
- **Polvo y Suciedad**: Limpiar el polvo y la suciedad de los componentes internos y externos del servidor utilizando aire comprimido y paños antiestáticos.
- **Ventiladores y Filtros**: Limpiar los ventiladores y filtros de aire para asegurar un flujo de aire adecuado.

**2. Verificación de Componentes**:
- **Inspección Visual**: Realizar inspecciones visuales periódicas para detectar signos de desgaste o daño en cables, conectores y componentes.
- **Temperatura y Voltaje**: Monitorizar las temperaturas y voltajes del sistema utilizando herramientas de hardware y software.

**3. Actualizaciones de Firmware y Controladores**:
- **Firmware**: Mantener actualizado el firmware de la placa base, controladores RAID, NIC y otros dispositivos.
- **Controladores**: Actualizar los controladores de hardware en el sistema operativo para asegurar compatibilidad y rendimiento óptimo.

#### Mantenimiento Correctivo

**1. Diagnóstico de Problemas**:
- **Herramientas de Diagnóstico**: Utilizar herramientas de diagnóstico para identificar fallos de hardware, como Memtest86 para la memoria RAM y herramientas SMART para discos duros.
- **Logs del Sistema**: Revisar los registros del sistema y los eventos para identificar posibles problemas de hardware.

**2. Reemplazo de Componentes**:
- **Componentes Defectuosos**: Reemplazar componentes defectuosos como módulos de RAM, discos duros y ventiladores con piezas nuevas o de repuesto.
- **Procedimientos de Reemplazo**: Seguir procedimientos adecuados para el reemplazo de componentes para evitar daños y asegurar la correcta reinstalación.

#### Planificación y Documentación

**1. Inventario de Hardware**:
- **Registro de Componentes**: Mantener un inventario detallado de todos los componentes de hardware del servidor, incluyendo modelos, números de serie y fechas de instalación.
- **Historial de Mantenimiento**: Documentar todas las actividades de mantenimiento, actualizaciones y reemplazos de hardware.

**2. Plan de Contingencia**:
- **Redundancia y Respaldo**: Implementar redundancia en componentes críticos como fuentes de alimentación y discos duros (RAID) y mantener respaldos regulares de datos.
- **Procedimientos de Recuperación**: Desarrollar y probar procedimientos de recuperación en caso de fallos de hardware para minimizar el tiempo de inactividad.
