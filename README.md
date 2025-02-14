# Microevaluacion

en este caso instalaremos lo que es msqlserver
Requisitos previos
Tener Docker instalado en tu sistema
Tener acceso a PowerShell o una terminal de tu preferencia
# Pasos para la instalación
Verificación de WSL
Habilitar WSL en Windows
Abre PowerShell como Administrador.

Ejecuta el siguiente comando para habilitar WSL: Abre PowerShell como Administrador y ejecuta el siguiente comando para habilitar WSL:

powershell wsl --install Esto instalará WSL y descargará la distribución predeterminada (Ubuntu).

# Verificación de WSL

Verificación de WSL Una vez reiniciado, puedes verificar que WSL está instalado correctamente ejecutando el siguiente comando en PowerShell:

powershell powershell wsl -l -v

# Instalación de Docker

 Si aún no tienes Docker instalado, descárgalo e instálalo desde su sitio oficial. Una vez instalado Docker, asegúrate de que esté funcionando correctamente ejecutando el siguiente comando en PowerShell:

powershell powershell docker --version 3. Descarga de la Imagen de SQL Server

Descarga de la Imagen de SQL Server
Para usar SQL Server en Docker, necesitas descargar la imagen oficial de Microsoft SQL Server desde Docker Hub. El siguiente comando descarga la imagen más reciente de SQL Server 2022:

powershell powershell docker pull mcr.microsoft.com/mssql/server:2022-latest

# +Crear y Ejecutar el Contenedor de SQL Server
Para crear un contenedor de SQL Server, ejecuta el siguiente comando en PowerShell. Esto creará un contenedor con el nombre sqlserver y expondrá el puerto 1433 (puerto predeterminado de SQL Server):

powershell docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=yourStrong#Password" -p 1433:1433 --name sqlserver -d mcr.microsoft.com/mssql/server:2022-latest

Verificación de la Ejecución del Contenedor
Para verificar que el contenedor está en ejecución, usa el siguiente comando:

powershell powershell docker ps

Este comando te mostrará los contenedores en ejecución y te confirmará que SQL Server está corriendo correctamente.


