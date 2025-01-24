# **HOLA ME PRESENTO SOY WIN 10 Y WIN 11**

## **Arquitectura del Sistema Operativo de Windows**

### **Capas principales**

**Hardware Abstraction Layer (HAL)**: Intermediario entre hardware y sistema operativo.  
**Kernel Mode**: Nivel más privilegiado, gestiona recursos críticos.  
**User Mode**: Para aplicaciones y servicios no críticos, aislando fallos del sistema.

## **Seguridad y aislamiento**
* **Modos de operación**: El Kernel Mode maximiza eficiencia en operaciones críticas; el User Mode limita riesgos de vulnerabilidades.  
* **Paginación y memoria virtual**: Aseguran aislamiento entre procesos y optimizan uso de RAM.

## Por su propósito

| **Criterio de clasificación** | **Tipo de SO**     | **Descripción**                                         | **Ejemplos**                                  |
|-------------------------------|--------------------|---------------------------------------------------------|-----------------------------------------------|
| **SO de escritorio**           | Diseñados para usuarios finales en PCs o laptops.    | Windows, macOS, Linux (Ubuntu, Mint)                |
## Por su núcleo (kernel)
|-------------------------------|--------------------|---------------------------------------------------------|-----------------------------------------------|
| **Híbrido**                   | Combina características de otros modelos.           | Windows NT, macOS                                |

El núcleo de Windows es **híbrido**, combinando ventajas de microkernels (modularidad y seguridad) y monolíticos (rendimiento).
* **WOW64**: Subsistema que permite ejecutar aplicaciones de 32 bits en entornos de 64 bits.  
* **Memoria**: Modelo de paginación para mapear direcciones físicas y virtuales; aislamiento de aplicaciones.

## Por su licencia
|-------------------------------|--------------------|---------------------------------------------------------|-----------------------------------------------|
| **Propietarios**              | Requieren licencia y no permiten acceso al código.  | Windows, macOS                                    |

## Por su interfaz
|-------------------------------|--------------------|---------------------------------------------------------|-----------------------------------------------|
| **Gráfica**                   | Interacción mediante GUI.                          | Windows, macOS                                   |

## Por su arquitectura soportada
|-------------------------------|--------------------|---------------------------------------------------------|-----------------------------------------------|
| **x86/x64**                   | Para PCs tradicionales.                              | Windows, Linux                                   |

## **Diferencias técnicas entre Windows 10 y Windows 11**

# Comparativa: Windows 10 vs. Windows 11

| **Característica**                  | **Windows 10**                                                                 | **Windows 11**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **Lanzamiento**                     | Julio de 2015                                                                   | Octubre de 2021                                                                |
| **Interfaz de usuario**             | Diseño tradicional con Live Tiles.                                              | Diseño modernizado con esquinas redondeadas y barra de tareas centrada.        |
| **Requisitos mínimos de hardware**  | - Procesador: 1 GHz, 2 núcleos, 64 bits. <br> - RAM: 1 GB (32 bits), 2 GB (64 bits). <br> - TPM: No obligatorio. | - Procesador: 1 GHz, 2 núcleos, 64 bits (SoC compatible). <br> - RAM: 4 GB. <br> - TPM: 2.0 obligatorio. |
| **Menú Inicio**                     | Basado en Live Tiles, acceso directo a programas.                               | Diseño minimalista, sin Live Tiles. Agrupa apps recientes y recomendadas.     |
| **Soporte para apps Android**       | No soporta apps Android nativamente.                                            | Soporte nativo a través de Amazon Appstore (requiere subsistema Android).      |
| **Multitarea**                      | Soporte básico para dividir ventanas manualmente.                              | Mejora con Snap Layouts y Snap Groups para organizar ventanas.                 |
| **Gaming**                          | Compatible con DirectX 12 y AutoHDR limitado.                                   | Mejor soporte para DirectX 12 Ultimate, AutoHDR y DirectStorage.               |
| **Microsoft Teams**                 | Aplicación opcional descargable.                                               | Integración nativa en la barra de tareas.                                      |
| **Actualizaciones**                 | Ciclo regular de 2 actualizaciones anuales.                                     | Actualizaciones anuales, optimizadas y más rápidas.                            |
| **Compatibilidad con hardware antiguo** | Compatible con una amplia gama de dispositivos.                               | Requiere hardware más reciente.                                                |
| **Widgets**                         | No disponibles.                                                                | Panel de widgets para noticias, clima y contenido personalizado.               |
| **Seguridad**                       | Soporte para TPM 1.2 y Secure Boot opcional.                                    | Requiere TPM 2.0, Secure Boot y aislamiento de hardware.                       |
| **Barra de tareas**                 | Personalizable y admite arrastrar y soltar.                                    | Menos personalizable (al inicio); sin arrastrar y soltar (reintroducido más tarde). |
| **Explorador de archivos**          | Diseño tradicional con cinta (ribbon).                                         | Rediseño con menos opciones visibles y botones minimalistas.                   |
| **Virtualización**                  | Hyper-V y Windows Sandbox opcionales.                                          | Mejor soporte para tecnologías modernas de virtualización.                     |

## **Sistema de carpetas en Windows**

| **Carpeta**                         | **Descripción**                                                                 |
|-------------------------------------|---------------------------------------------------------------------------------|
| `C:\Windows`                        | Carpeta principal del sistema operativo, contiene archivos esenciales de Windows. |
| `C:\Windows\System32`               | Contiene archivos esenciales del sistema, como ejecutables, bibliotecas DLL y herramientas del sistema. |
| `C:\Windows\SysWOW64`               | Contiene bibliotecas y ejecutables de 32 bits en sistemas operativos de 64 bits. |
| `C:\Windows\Temp`                   | Archivos temporales generados por el sistema y aplicaciones. Se puede limpiar regularmente. |
| `C:\Windows\System32\drivers`       | Almacena los controladores de dispositivos del sistema.                        |
| `C:\Windows\Fonts`                  | Contiene las fuentes del sistema utilizadas por las aplicaciones.             |
| `C:\Program Files`                  | Carpeta por defecto para las aplicaciones de 64 bits instaladas en el sistema. |
| `C:\Program Files (x86)`            | Carpeta destinada a las aplicaciones de 32 bits instaladas en sistemas de 64 bits. |
| `C:\Users\<Usuario>`                | Carpeta del perfil de usuario, que contiene documentos, configuraciones y archivos de la cuenta. |
| `C:\Users\<Usuario>\Documents`      | Carpeta personal para almacenar documentos del usuario.                       |
| `C:\Users\<Usuario>\Downloads`      | Carpeta predeterminada para los archivos descargados de Internet.             |
| `C:\Users\<Usuario>\Pictures`       | Carpeta predeterminada para imágenes y fotos del usuario.                     |
| `C:\Users\<Usuario>\Videos`         | Carpeta predeterminada para videos del usuario.                               |
| `C:\Users\<Usuario>\Desktop`        | Carpeta que contiene los accesos directos y archivos en el escritorio del usuario. |
| `C:\Users\<Usuario>\AppData`        | Carpeta oculta que contiene datos de aplicaciones y configuraciones específicas del usuario. |
| `C:\Users\<Usuario>\AppData\Local`  | Contiene datos y configuraciones de las aplicaciones instaladas en el equipo. |
| `C:\Users\<Usuario>\AppData\Roaming`| Almacena configuraciones y archivos de aplicaciones que son sincronizados entre dispositivos. |
| `C:\Users\<Usuario>\AppData\LocalLow`| Contiene configuraciones de aplicaciones de bajo nivel (por ejemplo, aplicaciones de navegador web). |
| `C:\ProgramData`                    | Carpeta utilizada por programas para almacenar datos de aplicación compartidos entre todos los usuarios. |
| `C:\Windows\Prefetch`               | Carpeta que almacena archivos utilizados para acelerar el arranque de las aplicaciones. |
| `C:\Windows\Installer`              | Carpeta que contiene los archivos de instalación de aplicaciones y actualizaciones del sistema. |
| `C:\$Recycle.Bin`                   | Carpeta que contiene los archivos eliminados temporalmente antes de su eliminación definitiva (Papelera de reciclaje). |
| `C:\Recovery`                       | Carpeta oculta utilizada para almacenar archivos necesarios para la recuperación del sistema. |
| `C:\Program Files\Common Files`     | Carpeta utilizada por programas para almacenar archivos compartidos entre aplicaciones. |
| `C:\Program Files\WindowsApps`      | Carpeta donde se almacenan las aplicaciones de la Tienda de Windows (Windows Store). |
| `C:\Windows\Logs`                   | Carpeta que contiene archivos de registro del sistema y las aplicaciones.     |
| `C:\Windows\en-US`                  | Carpeta que contiene los archivos de localización y recursos de idioma en inglés de Estados Unidos. |
| `C:\Windows\Web`                    | Carpeta que contiene fondos de pantalla predeterminados y otros recursos gráficos del sistema. |
| `C:\Windows\System32\wbem`          | Contiene archivos relacionados con la administración de Windows Management Instrumentation (WMI). |
| `C:\Windows\System32\LogFiles`      | Carpeta que almacena los archivos de registro del sistema.                    |
| `C:\Windows\System32\GroupPolicy`   | Carpeta que contiene políticas de grupo que definen configuraciones de seguridad y administrativas. |
| `C:\Windows\System32\Tasks`         | Almacena las tareas programadas del sistema y aplicaciones.                   |
| `C:\Windows\System32\drivers\etc`   | Carpeta que contiene archivos esenciales para la configuración de red, como el archivo `hosts`. |
| `C:\Windows\System32\config`        | Almacena las configuraciones del registro de Windows.                         |
| `C:\Windows\System32\ras`           | Contiene archivos relacionados con la funcionalidad de red, incluyendo las conexiones VPN. |
| `C:\Windows\System32\spool`         | Carpeta usada para almacenar trabajos de impresión pendientes.                |
| `C:\Windows\System32\catroot`       | Carpeta que se usa para almacenar los archivos relacionados con la firma digital. |
| `C:\Windows\System32\catroot2`      | Usada por el sistema de actualizaciones de Windows para almacenar certificados y archivos relacionados. |
| `C:\Windows\System32\FxsData`       | Carpeta utilizada por el servicio de fax en Windows.                          |
| `C:\Windows\Microsoft.NET`          | Carpeta donde se almacenan los archivos necesarios para el Framework .NET.    |
| `C:\Windows\servicing`              | Carpeta utilizada para almacenar archivos relacionados con la instalación de actualizaciones de Windows. |
| `C:\Windows\System32\wscsvc`        | Carpeta que almacena archivos relacionados con la función de Centro de Seguridad de Windows. |
| `C:\Windows\System32\FONTS`         | Carpeta donde se almacenan las fuentes del sistema operativo.                 |
| `C:\Program Files\Internet Explorer`| Carpeta que contiene archivos de la antigua versión de Internet Explorer.     |
| `C:\ProgramData\Microsoft\Windows\Start Menu` | Contiene accesos directos del menú de inicio. |
| `C:\Windows\System32\DRIVERS\UMDF`  | Contiene archivos relacionados con el marco de trabajo de drivers en modo usuario. |
| `C:\Windows\System32\spool\PRINTERS`| Carpeta usada para almacenar trabajos de impresión pendientes.                |
| `C:\Windows\System32\oobe`          | Contiene archivos relacionados con la experiencia de configuración inicial de Windows (Out of Box Experience). |
| `C:\Windows\System32\migwiz`        | Carpeta que almacena archivos necesarios para el asistente de transferencia de Windows. |
| `C:\Windows\System32\Printing_Admin_Scripts` | Contiene scripts relacionados con la administración de impresión en Windows. |
| `C:\Windows\System32\drivers\store` | Carpeta que contiene archivos relacionados con la configuración del almacén de drivers. |
| `C:\Windows\System32\winevt`        | Carpeta que contiene archivos de registro de eventos de Windows.             |
| `C:\Windows\System32\NDF`           | Contiene archivos relacionados con el diagnóstico de red y funcionalidad.    |
| `C:\Windows\System32\SoftwareDistribution` | Carpeta que contiene archivos de actualización de Windows. |
| `C:\Windows\System32\WinBioDatabase`| Carpeta que contiene la base de datos biométrica utilizada por Windows.      |
| `C:\Windows\System32\Wbem`          | Carpeta que contiene archivos del sistema de administración de Windows Management Instrumentation (WMI). |


## **Variables de entorno**
Las variables de entorno son valores dinámicos que pueden afectar la forma en que se ejecutan los procesos en un sistema 
operativo. Actúan como parámetros que informan a los programas y scripts sobre el entorno en el que se están ejecutando, 
proporcionando información importante sobre rutas de directorios, configuraciones de sistema, y más.

### Variables del Sistema

1. **`%SystemRoot%`**:
   - **Descripción**: Es la carpeta principal de instalación del sistema operativo Windows.
   - **Uso**: Se utiliza para localizar rápidamente archivos y carpetas del sistema sin necesidad de especificar la ruta completa. Normalmente apunta a `C:\Windows`.

2. **`%ProgramFiles%`**:
   - **Descripción**: Indica la carpeta predeterminada donde se instalan las aplicaciones de 64 bits.
   - **Uso**: Es útil para scripts y programas que necesitan acceder a archivos de aplicaciones instaladas sin importar dónde esté ubicado `C:\Program Files`.

3. **`%ProgramFiles(x86)%`**:
   - **Descripción**: Indica la carpeta predeterminada donde se instalan las aplicaciones de 32 bits en un sistema operativo de 64 bits.
   - **Uso**: Permite a los programas y scripts localizar la ubicación de las aplicaciones de 32 bits, típicamente en `C:\Program Files (x86)`.

4. **`%CommonProgramFiles%`**:
   - **Descripción**: Carpeta donde se almacenan archivos comunes compartidos por múltiples aplicaciones.
   - **Uso**: Facilita el acceso a componentes que son utilizados por varias aplicaciones, como librerías DLL.

### Variables del Usuario

1. **`%APPDATA%`**:
   - **Descripción**: Carpeta que contiene los datos de las aplicaciones específicas del usuario actual.
   - **Uso**: Facilita el almacenamiento y la recuperación de configuraciones y datos de aplicaciones que son específicos del usuario, normalmente apunta a `C:\Users\<Usuario>\AppData\Roaming`.

2. **`%LOCALAPPDATA%`**:
   - **Descripción**: Almacena los datos específicos del usuario que no necesitan ser sincronizados con otros dispositivos.
   - **Uso**: Permite a las aplicaciones guardar configuraciones locales, normalmente apunta a `C:\Users\<Usuario>\AppData\Local`.

3. **`%USERPROFILE%`**:
   - **Descripción**: Es la carpeta principal del perfil del usuario actual.
   - **Uso**: Se utiliza para acceder rápidamente a las carpetas específicas del usuario, como Escritorio, Documentos, Descargas, etc. Normalmente apunta a `C:\Users\<Usuario>`.

4. **`%HOMEPATH%`**:
   - **Descripción**: Ruta de la carpeta principal del usuario.
   - **Uso**: Similar a `%USERPROFILE%`, pero normalmente apunta directamente a `\Users\<Usuario>` sin la unidad de disco.

5. **`%HOMEDRIVE%`**:
   - **Descripción**: Unidad de disco donde se encuentra la carpeta del perfil del usuario.
   - **Uso**: Junto con `%HOMEPATH%` para formar la ruta completa de la carpeta del perfil del usuario. Por ejemplo, `C:`.

### Otras Variables Útiles

1. **`%TEMP%`** / **`%TMP%`**:
   - **Descripción**: Rutas a las carpetas temporales del usuario actual.
   - **Uso**: Utilizadas por aplicaciones para almacenar archivos temporales. Normalmente apunta a `C:\Users\<Usuario>\AppData\Local\Temp`.

2. **`%WINDIR%`**:
   - **Descripción**: Es una alternativa a `%SystemRoot%`, señalando la carpeta de instalación de Windows.
   - **Uso**: Permite a las aplicaciones y scripts localizar archivos del sistema Windows de manera consistente.

## **Comandos y Programas de Windows**

| **Comando/Programa**        | **Descripción**                                                                 |
|-----------------------------|---------------------------------------------------------------------------------|
| `cmd`                       | Línea de comandos de Windows, permite ejecutar programas y scripts en modo texto.|
| `powershell`                | Shell avanzada y lenguaje de secuencias de comandos, más potente que `cmd`.     |
| `explorer`                  | Abre el explorador de archivos de Windows para gestionar archivos y carpetas.  |
| `msconfig`                  | Configuración del sistema para ajustar el inicio y los servicios del sistema.  |
| `taskmgr`                   | Abre el Administrador de tareas para gestionar procesos y aplicaciones.        |
| `regedit`                   | Editor del Registro de Windows para modificar configuraciones avanzadas del sistema.|
| `winver`                    | Muestra la versión del sistema operativo Windows.                              |
| `chkdsk`                    | Comando para verificar el estado del disco duro y reparar errores del sistema de archivos.|
| `ipconfig`                  | Muestra la configuración de la red de Windows, como direcciones IP y máscaras de subred.|
| `ping`                      | Herramienta de red que verifica la conectividad entre dispositivos mediante paquetes de datos.|
| `tracert`                   | Muestra la ruta que siguen los paquetes hasta un destino, útil para diagnosticar problemas de red.|
| `netstat`                   | Muestra estadísticas de red, incluyendo conexiones activas y puertos en uso.   |
| `sfc `   *****              | Comando que verifica la integridad de los archivos del sistema y los repara si es necesario.|
| `tasklist`                  | Muestra todos los procesos en ejecución en el sistema.                         |
| `taskkill`                  | Permite terminar un proceso o una aplicación específica desde la línea de comandos.|
| `systeminfo`  *****         | Muestra información detallada sobre el sistema operativo y hardware.          |
| `secpol.msc`                | Abre la Consola de seguridad local para configurar políticas de seguridad.     |
| `gpedit.msc`                | Editor de directivas de grupo para administrar políticas de seguridad y configuraciones avanzadas.|
| `firewall.cpl`              | Abre la configuración del firewall de Windows.                                 |
| `devmgmt.msc`               | Abre el Administrador de dispositivos para gestionar hardware conectado al sistema.|
| `control userpasswords2`    | Configura las contraseñas de usuario y las opciones de inicio automático.      |
| `cleanmgr`                  | Herramienta para liberar espacio en disco eliminando archivos temporales y otros elementos innecesarios.|
| `secpol.msc`                | Consola para políticas de seguridad en un sistema local o dominio.            |
| `gpresult`                  | Muestra el resultado de las políticas de grupo aplicadas en el sistema.        |
| `wbemtest`                  | Herramienta de diagnóstico de WMI (Instrumental de administración de Windows).  |
| `rasphone`                  | Herramienta para configurar conexiones de acceso remoto y VPN.                |
| `compmgmt.msc`              | Abre la Administración de equipos, una herramienta de administración centralizada.|
| `sdclt`                     | Abre la herramienta de copia de seguridad y restauración de Windows.           |
| `hdwwiz.cpl`                | Asistente para la instalación de nuevo hardware en el sistema.                 |
| `sysdm.cpl`                 | Configuración del sistema, donde se ajustan configuraciones de hardware, nombre de equipo, etc.|
| `wf.msc`    ******          | Abre la consola de configuración avanzada del Firewall de Windows.            |
| `wsreset`                   | Resetea la Tienda de Windows, útil si la tienda no funciona correctamente.     |
| `winrm`                     | Configura y gestiona la administración remota de Windows.                      |
| `wfs`                       | Herramienta de administración de servicios de Windows.                        |
| `lusrmgr.msc`               | Herramienta para la gestión de cuentas de usuario y grupos locales.   
| `diskpart`                  | Herramienta para la gestión de discos duros y particiones desde la línea de comandos.|
| `taskschd.msc`              | Abre el Programador de tareas para gestionar tareas automáticas en Windows.    |
| `certmgr.msc`               | Abre el Administrador de certificados para gestionar certificados digitales.  |
| `printmanagement.msc`       | Abre la administración de impresoras y colas de impresión.                     |
| `eventvwr.msc` *****        | Abre el Visor de eventos para analizar los logs del sistema y las aplicaciones.|
| `winver`                    | Muestra la versión de Windows instalada en el sistema.                        |
| `shutdown`                  | Comando para apagar o reiniciar el sistema.                                    |
| `control`                   | Abre el Panel de control de Windows.                                           |
| `win + R`                   | Abre la ventana de "Ejecutar" para ejecutar programas y comandos rápidamente.   |
| `eventvwr`                  | Abre el Visor de eventos, donde se pueden revisar los registros del sistema y aplicaciones.|
| `lusrmgr.msc`               | Gestiona las cuentas de usuario y grupos locales del sistema.              |
| `diskmgmt.msc`              | Gestiona particiones y volúmenes del sistema de almacenamiento.              |
| `msconfig`                  | Administra servicios y programas de inicio del sistema.                     |
| `resmon`                    | Monitorea el uso de CPU, RAM, disco y red en tiempo real.                    |
| `mrt`                       | Abre el antivirus de windows                                                 |


## SOFTWARE DE MANTENIMIENTO DESCARGABLE Y OFICIAL DE Microsoft

# Sysinternals Suite

# Sysinternals Suite - Herramientas completas

La Sysinternals Suite es un conjunto de herramientas avanzadas para solucionar problemas y optimizar sistemas Windows.  
Puedes descargarla desde el sitio oficial:  
[Descargar Sysinternals Suite](https://learn.microsoft.com/en-us/sysinternals/downloads/sysinternals-suite)

| **Herramienta**            | **Descripción**                                                                                                                                             | **Enlace**                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **AccessChk**               | Verifica los permisos efectivos en archivos, carpetas, claves de registro y otros objetos del sistema.                                                     | [AccessChk](https://learn.microsoft.com/en-us/sysinternals/downloads/accesschk)                              |
| **AccessEnum**   *****      | Muestra los permisos de acceso efectivos de archivos y carpetas de una manera fácil de entender.                                                           | [AccessEnum](https://learn.microsoft.com/en-us/sysinternals/downloads/accessenum)                            |
| **ADExplorer**              | Explora y edita la base de datos de Active Directory.                                                                                                      | [ADExplorer](https://learn.microsoft.com/en-us/sysinternals/downloads/adexplorer)                            |
| **ADInsight**               | Realiza un seguimiento detallado de las consultas LDAP en tiempo real.                                                                                      | [ADInsight](https://learn.microsoft.com/en-us/sysinternals/downloads/adinsight)                              |
| **Autologon**               | Configura inicios de sesión automáticos sin necesidad de introducir credenciales manualmente.                                                              | [Autologon](https://learn.microsoft.com/en-us/sysinternals/downloads/autologon)                              |
| **Autoruns**                | Muestra programas configurados para ejecutarse automáticamente al inicio del sistema o sesión del usuario.                                                  | [Autoruns](https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns)                                |
| **BgInfo**                  | Personaliza el fondo de pantalla con información del sistema, como nombre del equipo, IP, memoria, etc.                                                     | [BgInfo](https://learn.microsoft.com/en-us/sysinternals/downloads/bginfo)                                    |
| **CacheSet**                | Permite ajustar el tamaño del caché de archivos en sistemas Windows.                                                                                       | [CacheSet](https://learn.microsoft.com/en-us/sysinternals/downloads/cacheset)                                |
| **ClockRes**                | Muestra la resolución del temporizador del sistema.                                                                                                        | [ClockRes](https://learn.microsoft.com/en-us/sysinternals/downloads/clockres)                                |
| **Contig**                  | Desfragmenta archivos específicos en un disco para optimizar su rendimiento.                                                                               | [Contig](https://learn.microsoft.com/en-us/sysinternals/downloads/contig)                                    |
| **Coreinfo**                | Muestra información detallada sobre la arquitectura del procesador y las capacidades del sistema.                                                          | [Coreinfo](https://learn.microsoft.com/en-us/sysinternals/downloads/coreinfo)                                |
| **Ctrl2cap**                | Permite remapear la tecla Caps Lock como Ctrl.                                                                                                             | [Ctrl2cap](https://learn.microsoft.com/en-us/sysinternals/downloads/ctrl2cap)                                |
| **DebugView**               | Captura información de depuración en tiempo real en un sistema local o remoto.                                                                             | [DebugView](https://learn.microsoft.com/en-us/sysinternals/downloads/debugview)                              |
| **Desktops**                | Habilita el uso de escritorios virtuales en Windows.                                                                                                       | [Desktops](https://learn.microsoft.com/en-us/sysinternals/downloads/desktops)                                |
| **Disk2vhd**                | Convierte discos físicos en archivos de disco virtual (VHD).                                                                                               | [Disk2vhd](https://learn.microsoft.com/en-us/sysinternals/downloads/disk2vhd)                                |
| **DiskExt**                 | Muestra detalles de las particiones y discos físicos.                                                                                                     | [DiskExt](https://learn.microsoft.com/en-us/sysinternals/downloads/diskext)                                  |
| **DiskMon**                 | Monitoriza la actividad del disco en tiempo real.                                                                                                          | [DiskMon](https://learn.microsoft.com/en-us/sysinternals/downloads/diskmon)                                  |
| **DU (Disk Usage)**         | Muestra el uso del espacio en disco para una carpeta específica.                                                                                           | [DU](https://learn.microsoft.com/en-us/sysinternals/downloads/du)                                            |
| **EFSDump**                 | Muestra detalles sobre los archivos cifrados con EFS (Encrypting File System).                                                                             | [EFSDump](https://learn.microsoft.com/en-us/sysinternals/downloads/efsdump)                                  |
| **Handle**                  | Muestra información sobre handles abiertos por procesos.                                                                                                  | [Handle](https://learn.microsoft.com/en-us/sysinternals/downloads/handle)                                    |
| **Hex2dec**                 | Convierte números entre formatos hexadecimal y decimal.                                                                                                   | [Hex2dec](https://learn.microsoft.com/en-us/sysinternals/downloads/hex2dec)                                  |
| **Junction**                | Crea y gestiona enlaces simbólicos (junctions) en el sistema de archivos NTFS.                                                                             | [Junction](https://learn.microsoft.com/en-us/sysinternals/downloads/junction)                                |
| **ListDLLs**                | Muestra las DLL cargadas en memoria por los procesos activos.                                                                                              | [ListDLLs](https://learn.microsoft.com/en-us/sysinternals/downloads/listdlls)                                |
| **LiveKd**                  | Permite realizar análisis de depuración en sistemas en vivo utilizando imágenes de memoria (dumps).                                                        | [LiveKd](https://learn.microsoft.com/en-us/sysinternals/downloads/livekd)                                    |
| **LoadOrder**               | Muestra el orden de carga de los controladores en el sistema.                                                                                             | [LoadOrder](https://learn.microsoft.com/en-us/sysinternals/downloads/loadorder)                              |
| **LogonSessions**           | Muestra todas las sesiones activas de inicio de sesión en el sistema.                                                                                     | [LogonSessions](https://learn.microsoft.com/en-us/sysinternals/downloads/logonsessions)                      |
| **MoveFile**                | Programa el movimiento o eliminación de archivos durante el reinicio del sistema.                                                                          | [MoveFile](https://learn.microsoft.com/en-us/sysinternals/downloads/movefile)                                |
| **NotMyFault**              | Causa fallos deliberados en el sistema para probar herramientas de depuración.                                                                             | [NotMyFault](https://learn.microsoft.com/en-us/sysinternals/downloads/notmyfault)                            |
| **PendMoves**               | Muestra los archivos programados para ser movidos o eliminados en el próximo reinicio del sistema.                                                         | [PendMoves](https://learn.microsoft.com/en-us/sysinternals/downloads/pendmoves)                              |
| **PipeList**                | Muestra todos los pipes nombrados abiertos y sus propietarios.                                                                                            | [PipeList](https://learn.microsoft.com/en-us/sysinternals/downloads/pipelist)                                |
| **ProcDump**                | Genera volcados de memoria (dumps) de procesos, útil para diagnósticos y análisis de errores.                                                              | [ProcDump](https://learn.microsoft.com/en-us/sysinternals/downloads/procdump)                                |
| **Process Explorer**  ***** | Proporciona información detallada sobre procesos activos, DLL y handles abiertos.                                                                          | [Process Explorer](https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer)                |
| **Process Monitor**   ***** | Realiza seguimiento en tiempo real de actividad del sistema de archivos, registro, procesos y red.                                                         | [Process Monitor](https://learn.microsoft.com/en-us/sysinternals/downloads/procmon)                          |
| **PsExec**                  | Ejecuta procesos de forma remota y permite abrir shells remotas.                                                                                          | [PsExec](https://learn.microsoft.com/en-us/sysinternals/downloads/psexec)                                    |
| **PsFile**                  | Muestra archivos abiertos en recursos compartidos remotos.                                                                                                | [PsFile](https://learn.microsoft.com/en-us/sysinternals/downloads/psfile)                                    |
| **PsKill**                  | Finaliza procesos en equipos locales o remotos.                                                                                                           | [PsKill](https://learn.microsoft.com/en-us/sysinternals/downloads/pskill)                                    |
| **RAMMap**                  | Proporciona un desglose detallado del uso de la memoria física del sistema.                                                                                | [RAMMap](https://learn.microsoft.com/en-us/sysinternals/downloads/rammap)                                    |
| **RegDelNull**              | Busca y elimina claves de registro con nombres nulos.                                                                                                     | [RegDelNull](https://learn.microsoft.com/en-us/sysinternals/downloads/regdelnull)                            |
| **RootkitRevealer** *****   | Detecta rootkits en el sistema mediante análisis de discrepancias en el sistema de archivos y registro.                                                    | [RootkitRevealer](https://learn.microsoft.com/en-us/sysinternals/downloads/rootkit-revealer)                 |
| **SigCheck**                | Verifica las firmas digitales de archivos y consulta información de reputación en línea.                                                                   | [SigCheck](https://learn.microsoft.com/en-us/sysinternals/downloads/sigcheck)                                |
| **Streams**                 | Muestra flujos de datos alternativos (ADS) de archivos NTFS.                                                                                              | [Streams](https://learn.microsoft.com/en-us/sysinternals/downloads/streams)                                  |
| **Strings**                 | Extrae cadenas de texto de archivos binarios.                                                                                                             | [Strings](https://learn.microsoft.com/en-us/sysinternals/downloads/strings)                                  |
| **Sync**                    | Fuerza a que las cachés de disco se sincronicen con el sistema de archivos.                                                                                | [Sync](https://learn.microsoft.com/en-us/sysinternals/downloads/sync)                                        |
| **TCPView**    *****        | Muestra una lista de conexiones TCP y UDP activas junto con los procesos asociados.                                                                        | [TCPView](https://learn.microsoft.com/en-us/sysinternals/downloads/tcpview)                                  |
| **VMMap**                   | Proporciona un desglose detallado del uso de memoria de un proceso específico.                                                                             | [VMMap](https://learn.microsoft.com/en-us/sysinternals/downloads/vmmap)                                      |
| **Whois**                   | Realiza búsquedas WHOIS para obtener información sobre dominios y direcciones IP.                                                                          | [Whois](https://learn.microsoft.com/en-us/sysinternals/downloads/whois)                                      |
| **WinObj**                  | Muestra el espacio de nombres del objeto NT del sistema.                                                                                                  | [WinObj](https://learn.microsoft.com/en-us/sysinternals/downloads/winobj)                                    |
| **ZoomIt**     ******       | Permite hacer zoom y realizar anotaciones en pantalla durante presentaciones.                                                                              | [ZoomIt](https://learn.microsoft.com/en-us/sysinternals/downloads/zoomit)                                    |

## Notas
1. Algunas herramientas requieren privilegios de administrador.
2. Las utilidades se pueden ejecutar sin instalación, lo que las hace portables.

# **Resolución de Problemas Comunes**

## 1. **BSOD (Pantallas Azules de la Muerte)**

Las **Pantallas Azules de la Muerte (BSOD)** son errores críticos del sistema que requieren atención inmediata para evitar la pérdida de datos y mejorar la estabilidad del sistema.
A continuación, se detallan las causas comunes y soluciones para abordar estos errores.

# BSOD Más Comunes en Windows

| **Código de error** | **Nombre del error**                 | **Causa común**                                                                                 | **Posible solución**                                                                                       |
|----------------------|--------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **0x0000000A**       | `IRQL_NOT_LESS_OR_EQUAL`            | Controladores incompatibles, problemas de hardware o acceso incorrecto a memoria.              | - Actualiza los controladores.<br>- Verifica el hardware RAM.<br>- Usa herramientas como **Memtest86**.    |
| **0x0000001E**       | `KMODE_EXCEPTION_NOT_HANDLED`       | Controladores defectuosos o problemas en software.                                             | - Actualiza Windows y controladores.<br>- Revisa aplicaciones recientes.                                   |
| **0x00000050**       | `PAGE_FAULT_IN_NONPAGED_AREA`       | Problemas con la memoria RAM o software que accede a ubicaciones de memoria incorrectas.       | - Ejecuta un diagnóstico de memoria.<br>- Desactiva software recién instalado.                            |
| **0x0000007B**       | `INACCESSIBLE_BOOT_DEVICE`          | Cambios en la configuración del disco (AHCI/IDE), archivos de arranque corruptos o malware.    | - Verifica el modo SATA en la BIOS.<br>- Restaura el sistema o repara el sector de arranque.               |
| **0x0000007E**       | `SYSTEM_THREAD_EXCEPTION_NOT_HANDLED` | Problemas con controladores de hardware o software incompatible.                               | - Identifica el archivo relacionado al error en los detalles del BSOD.<br>- Actualiza o reinstala controladores. |
| **0x0000009F**       | `DRIVER_POWER_STATE_FAILURE`        | Controladores de dispositivos con problemas en la gestión de energía.                          | - Actualiza controladores.<br>- Configura opciones de energía para no suspender dispositivos críticos.     |
| **0x00000024**       | `NTFS_FILE_SYSTEM`                  | Corrupción en el sistema de archivos NTFS o errores en el disco.                               | - Ejecuta **chkdsk /f /r**.<br>- Verifica el estado del disco duro.                                        |
| **0x0000003B**       | `SYSTEM_SERVICE_EXCEPTION`          | Problemas de controladores, software o antivirus.                                              | - Reinstala controladores.<br>- Desactiva temporalmente el antivirus.                                      |
| **0x000000D1**       | `DRIVER_IRQL_NOT_LESS_OR_EQUAL`     | Controladores defectuosos que intentan acceder a memoria incorrecta.                           | - Identifica y actualiza controladores problemáticos.<br>- Usa el Visor de eventos para más detalles.      |
| **0x00000133**       | `DPC_WATCHDOG_VIOLATION`            | Problemas con controladores de disco o tiempos de espera excesivos en procesos.                | - Actualiza controladores de almacenamiento (SATA/NVMe).<br>- Revisa el estado del disco duro.             |
| **0x00000124**       | `WHEA_UNCORRECTABLE_ERROR`          | Error crítico de hardware, como CPU, RAM o disco duro.                                         | - Verifica el hardware con herramientas de diagnóstico.<br>- Comprueba temperaturas y overclocking.        |
| **0xC000021A**       | `STATUS_SYSTEM_PROCESS_TERMINATED`  | Fallo crítico en los procesos del sistema o corrupción de archivos esenciales.                 | - Repara archivos del sistema con **sfc /scannow**.<br>- Restaura el sistema a un punto anterior.          |

## Notas
- Algunos BSOD muestran archivos asociados al error. Usa herramientas como **BlueScreenView** para analizar los volcados de memoria (minidumps).
- Mantén el sistema actualizado y realiza copias de seguridad regulares para minimizar los riesgos.

Utiliza el **Administrador de dispositivos** (`devmgmt.msc`) para actualizar los controladores a sus versiones más recientes.
Utiliza la **Herramienta de Diagnóstico de Memoria de Windows** (`mdsched.exe`) o programas como **MemTest86** para verificar la integridad de la RAM.
**Comprobador de Archivos del Sistema**:
    - Ejecuta `sfc /scannow` en el símbolo del sistema para detectar y reparar archivos corruptos.
  - **Herramienta DISM**:
    - Ejecuta `DISM /Online /Cleanup-Image /RestoreHealth` para reparar la imagen del sistema.

# BONUS
BONUS DE INFORMACIÓN Descarga Win Original--- https://www.genbeta.com/windows/4-formas-descargar-iso-windows-10-gratis

Hacer una ISO "limpia" https://www.softzone.es/noticias/windows/crear-iso-windows-11-24h2-personal/

Mantenimiento SysInternals: https://learn.microsoft.com/es-es/sysinternals/ https://blogthinkbig.com/windows-sysinternals-pequenas-utilidades-para-tu-pc

Lo primero analizar lo que tiene instalado y valorar desinstalar programas innecesarios. Articulo de como hacer eso a mano --- https://www.xataka.com/basics/como-limpiar-windows-10-a-fondo-borra-que-no-necesitas-seguridad Ahora usando programas --- https://www.xataka.com/basics/mejores-aplicaciones-herramientas-gratis-para-limpiar-windows-10-formatear Valora el entorno y realiza pruebas, no sería la primera vez que un programa no es tan quirurgico como hacerlo a mano y rompe algo.

Sugerencias mejorar rendimiento WINDOWS de forma manual.

    https://support.microsoft.com/es-es/windows/sugerencias-para-mejorar-el-rendimiento-del-pc-en-windows-b3b3ef5b-5953-fb6a-2528-4bbed82fba96 

https://www.adslzone.net/esenciales/windows-10/trucos-acelerar-windows/

https://computerhoy.20minutos.es/windows/formas-rapidas-optimizar-maximo-pc-windows-11-1334092

Programas optimizar Windows de terceros

https://www.genbeta.com/a-fondo/estas-15-herramientas-gratis-que-siempre-instalo-para-administrar-optimizar-mi-sistema-windows

Opciones para limpiar a posteriori de Soft no necesario que se preinstala con Windows.:

https://www.xataka.com/basics/como-desinstalar-aplicaciones-preinstaladas-bloatware-windows-facilmente-solo-comando https://www.oo-software.com/en/ooappbuster https://github.com/nyxiereal/XToolbox

Herramientas PRO de analisis para mantenimiento de Windows son:

Hay que conocer : la de NirSoft y la de SysInternals y para manejarlas todas juntas como si fuesen un programa, lee el siguiente articulo. https://www.genbeta.com/herramientas/nirlauncher-lanzador-cientos-aplicaciones-portables-que-administrar-nuestro-sistema-windows

Con esto , tendrás una guía de windows y tooooodo lo que se puede tocar. OJITO con lo que rompes.

Mantenimiento Windows Server

Oficial --- https://learn.microsoft.com/es-es/windows-server/

Win Server 2022 -- https://learn.microsoft.com/es-es/windows-server/administration/performance-tuning/

Software de mantenimiento RECOMENDADO por mi. -Glary utilities

Software de mantenimiento RECOMENDADO por mi.
-Glary utilities



