# Sysinternals & Sysmon Auto-Installer

Este repositorio contiene un script de PowerShell (`Install_Sysinternal_Suite.ps1`) diseñado para automatizar la descarga, instalación y configuración de **Sysinternals Suite** y **Sysmon** con una configuración de seguridad optimizada (SwiftOnSecurity).

## Funcionalidades

*   **Portabilidad**: Se instala automáticamente en la unidad del sistema (ej. `C:\Sysinternals`), independiente de dónde se ejecute el script.
*   **Idempotencia**:
    *   Verifica si el servicio Sysmon ya está corriendo antes de intentar instalar.
    *   Verifica si los archivos de Sysinternals ya existen para evitar descargas innecesarias.
*   **Seguridad**: Requiere privilegios de Administrador para funcionar.
*   **Configuración**: Descarga y aplica automáticamente la configuración recomendada de [SwiftOnSecurity](https://github.com/SwiftOnSecurity/sysmon-config).

## Requisitos

*   Windows PowerShell 5.1 o superior.
*   Conexión a Internet (para la primera descarga).
*   Permisos de **Administrador**.

## Uso

1.  Abre PowerShell como Administrador.
2.  Navega a la carpeta donde está este script.
3.  Ejecuta el script:

```powershell
.\Install_Sysinternal_Suite.ps1
```

## Logs

Una vez instalado, los eventos de Sysmon se pueden visualizar en el Visor de Eventos de Windows bajo:
`Applications and Services Logs/Microsoft/Windows/Sysmon/Operational`
