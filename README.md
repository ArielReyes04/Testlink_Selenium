# Testlink_Selenium


# Testlink y Selenium - Guía de Instalación y Configuración

Este proyecto incluye los pasos necesarios para instalar y configurar **Testlink** y **Selenium** junto con una integración básica para su uso en un entorno local.

---

## Requisitos

1. **XAMPP**: Versión específica incluida en los archivos adjuntos.
2. **Python**: 
3. **Archivos del proyecto**: Carpetas **proyecto spa** y **testlink**.
4. **Conexión a internet**: Para instalar dependencias de Python.
Enlace de la version de XAMPP necesaria: https://www.mediafire.com/file/g9tuzz9qp6sqv0s/Ejecutables.zip/file
---

## Pasos de Instalación y Configuración

### 1. Preparación
1. Descargar y descomprimir la carpeta adjunta.
2. Verificar que se tienen todos los archivos necesarios.

### 2. Instalación de XAMPP
1. Instalar la versión de **XAMPP** incluida en los archivos adjuntos.
   - Si ya tienes una instalación previa de XAMPP, renombra la carpeta en el proceso de instalación para evitar conflictos con versiones previas.
   
### 3. Instalación de Python
1. Instalar la versión de **Python** incluida en la carpeta adjunta.
   - Asegúrate de **añadir Python al PATH** durante la instalación.

### 4. Configuración de Archivos
1. Copiar las carpetas **proyecto spa** y **testlink** a la carpeta `htdocs` de la instalación de XAMPP.

### 5. Configuración de XAMPP
1. Abrir el archivo `httpd.conf` ubicado en: [carpeta_XAMPP]/apache/conf/httpd.conf
2. Buscar la línea `AllowOverride` (línea 235) y cambiar `None` por `All`.
3. Guardar los cambios.

### 6. Configuración de Bases de Datos
1. Abrir **phpMyAdmin** con XAMPP activado.
2. Importar la base de datos:
- Crear una base de datos llamada **aura spa** (sin guiones).
- Importar el archivo SQL correspondiente.
3. Crear una nueva base de datos llamada **testlink**.

### 7. Instalación de Testlink
1. Acceder al enlace: http://localhost/testlink/
2. Realizar la instalación:
- Seleccionar **New Installation**.
- Aceptar los términos y condiciones.
- Continuar con los pasos hasta llegar a **Database admin login**:
  - Usuario: `root`
  - Contraseña: *(vacía)*
- En **TestLink DB login** y **Testlink DB password**, usar:
  - Usuario: `admin`
  - Contraseña: `admin`
- Hacer clic en **Process Testlink Setup!**.
3. Al finalizar, seleccionar el enlace bajo **Installation was successful**.
4. Iniciar sesión con:
- Usuario: `admin`
- Contraseña: `admin`.

### 8. Configuración de API en Testlink
1. Ir a **My Settings** -> **API Interface**.
2. Generar una nueva clave API seleccionando **Generate a new key**.

### 9. Instalación de Dependencias Python
1. Abrir una terminal (CMD) y ejecutar: "pip install selenium" y luego "pip install testlink-api-python-client"
- Debería mostrar un mensaje de conexión exitosa.

---

## Notas Finales

El entorno ahora está configurado y listo para su uso con Testlink y Selenium. Asegúrate de seguir las buenas prácticas para garantizar un correcto funcionamiento.

¡Buena suerte!
