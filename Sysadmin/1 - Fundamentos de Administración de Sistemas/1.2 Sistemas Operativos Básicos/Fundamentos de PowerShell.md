
#### Introducción a PowerShell

PowerShell es una plataforma de automatización y configuración de tareas desarrollada por Microsoft, que consiste en un shell de línea de comandos y un lenguaje de scripting. Diseñado inicialmente para la administración de sistemas, PowerShell permite a los administradores y profesionales de TI automatizar tareas y administrar configuraciones tanto en sistemas Windows como en otras plataformas.

**Características Clave de PowerShell**:
- **Integración Profunda con Windows**: PowerShell se integra profundamente con el sistema operativo Windows y los productos de Microsoft, facilitando la administración de sistemas y aplicaciones.
- **Objetos y Pipelining**: A diferencia de otros shells de comandos que manejan texto, PowerShell maneja objetos, lo que permite manipular y pasar datos complejos a través de comandos.
- **Extensibilidad**: PowerShell permite crear scripts y módulos personalizados, y se puede extender mediante cmdlets y funciones.
- **Compatibilidad Multiplataforma**: Con PowerShell Core (ahora conocido como PowerShell 7), Microsoft ha llevado PowerShell a ser multiplataforma, soportando Windows, macOS y Linux.

#### Primeros Pasos con PowerShell

**Ejecución de PowerShell**:
- **PowerShell en Windows**: PowerShell viene preinstalado en Windows. Se puede acceder a él buscando "PowerShell" en el menú Inicio.
- **PowerShell Core**: Para instalar PowerShell Core en Windows, macOS o Linux, se puede descargar desde la [página oficial de PowerShell](https://github.com/PowerShell/PowerShell).

**Comandos Básicos**:
- **Cmdlets**: Los comandos en PowerShell se llaman cmdlets (pronunciado "command-lets"). Un cmdlet es un comando ligero utilizado en el entorno de PowerShell.
- **Sintaxis**: La sintaxis básica de un cmdlet es `Verbo-Sustantivo`, como `Get-Process` o `Set-Item`.

**Ejemplos de Cmdlets Básicos**:
- `Get-Help`: Proporciona ayuda sobre cmdlets y conceptos de PowerShell.
  - Ejemplo: `Get-Help Get-Process`.
- `Get-Command`: Muestra una lista de todos los cmdlets disponibles.
  - Ejemplo: `Get-Command`.
- `Get-Process`: Lista todos los procesos en ejecución en el sistema.
  - Ejemplo: `Get-Process`.
- `Set-Location`: Cambia el directorio actual.
  - Ejemplo: `Set-Location C:\Users`.
- `Get-ChildItem`: Muestra los archivos y carpetas en el directorio actual.
  - Ejemplo: `Get-ChildItem`.

**Pipelining**:
- PowerShell permite pasar el resultado de un cmdlet como entrada para otro cmdlet mediante el uso del operador `|` (pipe).
  - Ejemplo: `Get-Process | Where-Object { $_.CPU -gt 100 }` (Obtiene todos los procesos que están utilizando más de 100 unidades de CPU).

#### Scripting y Automatización

**Creación de Scripts**:
- Los scripts de PowerShell se guardan en archivos con la extensión `.ps1`.
- Para ejecutar un script, se debe proporcionar la ruta completa o relativa al archivo del script.
  - Ejemplo: `.\script.ps1`.

**Variables**:
- Las variables en PowerShell se definen con el símbolo `$`.
  - Ejemplo: `$variable = "Hola, Mundo!"`.

**Estructuras de Control**:
- **If-Else**: Estructura condicional.
  - Ejemplo:
    ```powershell
    if ($condition) {
        Write-Output "Condition is true"
    } else {
        Write-Output "Condition is false"
    }
    ```
- **ForEach-Object**: Itera sobre cada elemento en una colección.
  - Ejemplo:
    ```powershell
    $items = Get-ChildItem
    $items | ForEach-Object { Write-Output $_.Name }
    ```
- **While**: Bucle que se ejecuta mientras la condición sea verdadera.
  - Ejemplo:
    ```powershell
    $counter = 0
    while ($counter -lt 10) {
        Write-Output $counter
        $counter++
    }
    ```

#### Administración del Sistema

**Gestión de Servicios**:
- **Get-Service**: Obtiene el estado de los servicios en el sistema.
  - Ejemplo: `Get-Service`.
- **Start-Service** y **Stop-Service**: Inicia y detiene servicios.
  - Ejemplo: `Start-Service -Name "Spooler"`.

**Administración de Usuarios**:
- **Get-LocalUser**: Lista todos los usuarios locales en el sistema.
  - Ejemplo: `Get-LocalUser`.
- **New-LocalUser**: Crea un nuevo usuario local.
  - Ejemplo: `New-LocalUser -Name "NewUser" -Password (ConvertTo-SecureString "Password123" -AsPlainText -Force) -FullName "New User"`.

**Gestión de Archivos y Directorios**:
- **New-Item**: Crea nuevos archivos o directorios.
  - Ejemplo: `New-Item -Path "C:\example" -ItemType "Directory"`.
- **Copy-Item**: Copia archivos o directorios.
  - Ejemplo: `Copy-Item -Path "C:\source.txt" -Destination "C:\destination.txt"`.
- **Remove-Item**: Elimina archivos o directorios.
  - Ejemplo: `Remove-Item -Path "C:\example" -Recurse`.

#### PowerShell Remoting

**Ejecución Remota**:
- PowerShell permite ejecutar comandos y scripts en computadoras remotas mediante PowerShell Remoting.
- **Enable-PSRemoting**: Habilita la ejecución remota en la computadora local.
  - Ejemplo: `Enable-PSRemoting -Force`.
- **Invoke-Command**: Ejecuta un comando en una o más computadoras remotas.
  - Ejemplo: `Invoke-Command -ComputerName "Server01" -ScriptBlock { Get-Process }`.

#### Módulos y Extensibilidad

**Uso de Módulos**:
- Los módulos en PowerShell son paquetes que contienen cmdlets, funciones, scripts y otros recursos.
- **Import-Module**: Importa un módulo a la sesión actual.
  - Ejemplo: `Import-Module -Name "ActiveDirectory"`.
- **Find-Module** y **Install-Module**: Encuentra e instala módulos desde el repositorio de PowerShell.
  - Ejemplo: `Find-Module -Name "AzureRM"`.
  - Ejemplo: `Install-Module -Name "AzureRM"`.

**Creación de Módulos Personalizados**:
- Los usuarios pueden crear sus propios módulos para organizar y compartir scripts y funciones.
- **Export-ModuleMember**: Define qué funciones y cmdlets se exportan del módulo.
  - Ejemplo:
    ```powershell
    Export-ModuleMember -Function Get-CustomFunction
    ```

#### Seguridad en PowerShell

**Políticas de Ejecución**:
- PowerShell tiene varias políticas de ejecución que determinan qué scripts se pueden ejecutar en el sistema.
- **Get-ExecutionPolicy**: Obtiene la política de ejecución actual.
  - Ejemplo: `Get-ExecutionPolicy`.
- **Set-ExecutionPolicy**: Cambia la política de ejecución.
  - Ejemplo: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`.

**Firmas de Scripts**:
- Los scripts pueden ser firmados digitalmente para asegurar su integridad y autenticidad.
- **Set-AuthenticodeSignature**: Firma un script con un certificado digital.
  - Ejemplo: `Set-AuthenticodeSignature -FilePath "script.ps1" -Certificate $cert`.

PowerShell es una herramienta poderosa y flexible que ha transformado la forma en que los administradores de sistemas y los profesionales de TI gestionan y automatizan sus entornos. Con un enfoque en la simplicidad, la extensibilidad y la integración profunda con el ecosistema de Microsoft, PowerShell sigue siendo una plataforma esencial para la administración moderna de sistemas.