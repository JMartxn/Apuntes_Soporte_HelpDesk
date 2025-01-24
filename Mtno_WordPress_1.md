# Guía de Seguridad para WordPress: Nginx vs Apache

A continuación se presenta una tabla detallada con los pasos a seguir para asegurar tu instalación de WordPress, especificando las configuraciones necesarias tanto para Nginx como para Apache.

| **Paso**                             | **Nginx**                                                                                                     | **Apache**                                                                                                    |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **1. Actualiza Todo**                | - **WordPress**: Mantén siempre la última versión desde el panel de administración.<br>- **Temas y Plugins**: Actualiza regularmente. | - **WordPress**: Mantén siempre la última versión desde el panel de administración.<br>- **Temas y Plugins**: Actualiza regularmente. |
| **2. Configura el Servidor**         | - **Archivo de configuración**: Edita el archivo de configuración de Nginx, típicamente ubicado en `/etc/nginx/sites-available/tu_dominio`.<br>- **Deshabilita listado de directorios**: `<br>autoindex off;`<br>- **Protege wp-config.php**: `<br>location ~* wp-config.php {<br> deny all;<br>}` | - **Archivo .htaccess**: Crea o edita el archivo `.htaccess` en el directorio raíz de WordPress (`/var/www/html/tu_dominio/.htaccess`).<br>- **Deshabilita listado de directorios**: `<br>Options -Indexes`<br>- **Protege wp-config.php**: `<br><files wp-config.php><br> Deny from all<br></files>` |
| **3. Asegura Permisos**              | - **Permisos de directorios**: Ejecuta `find /var/www/html/tu_dominio -type d -exec chmod 755 {} \;`<br>- **Permisos de archivos**: Ejecuta `find /var/www/html/tu_dominio -type f -exec chmod 644 {} \;` | - **Permisos de directorios**: Ejecuta `find /var/www/html/tu_dominio -type d -exec chmod 755 {} \;`<br>- **Permisos de archivos**: Ejecuta `find /var/www/html/tu_dominio -type f -exec chmod 644 {} \;` |
| **4. Configura un Firewall**         | - **UFW**: Ejecuta `sudo ufw allow 'Nginx Full'` para permitir tráfico HTTP y HTTPS.<br>- **Fail2ban**: Instala y configura usando `sudo apt install fail2ban`. | - **UFW**: Ejecuta `sudo ufw allow 'Apache Full'` para permitir tráfico HTTP y HTTPS.<br>- **Fail2ban**: Instala y configura usando `sudo apt install fail2ban`. |
| **5. Desactiva XML-RPC**             | - **Archivo de configuración**: Edita el archivo de configuración de Nginx.<br>- **Desactivar XML-RPC**: `<br>location = /xmlrpc.php {<br> deny all;<br>}` | - **Archivo .htaccess**: Agrega lo siguiente:<br><br>`<Files xmlrpc.php><br> Deny from all<br></Files>` |
| **6. Implementa HTTPS**              | - **Certificado SSL**: Usa Let's Encrypt.<br>- **Redirigir HTTP a HTTPS**: Agrega en el archivo de configuración de Nginx: `<br>server {<br> listen 80;<br> server_name tu_dominio.com www.tu_dominio.com;<br> return 301 https://$host$request_uri;<br>}` | - **Certificado SSL**: Usa Let's Encrypt.<br>- **Redirigir HTTP a HTTPS**: Agrega en el archivo de configuración de Apache: `<br><VirtualHost *:80><br> ServerName tu_dominio.com<br> ServerAlias www.tu_dominio.com<br> Redirect permanent / https://tu_dominio.com/<br></VirtualHost>` |
| **7. Usa Plugins de Seguridad**      | - **Plugins recomendados**: Instala Wordfence o iThemes Security desde el panel de administración de WordPress.<br> Asegúrate de configurar las opciones de firewall y escaneo. | - **Plugins recomendados**: Instala Wordfence o iThemes Security desde el panel de administración de WordPress.<br> Asegúrate de configurar las opciones de firewall y escaneo. |
| **8. Realiza Copias de Seguridad**   | - **Copia de Seguridad Regular**: Usa plugins como UpdraftPlus o BackWPup para realizar copias automáticas de la base de datos y archivos. Configura el almacenamiento en la nube si es posible. | - **Copia de Seguridad Regular**: Usa plugins como UpdraftPlus o BackWPup para realizar copias automáticas de la base de datos y archivos. Configura el almacenamiento en la nube si es posible. |
| **9. Monitorea Tu Sitio**            | - **Herramientas de Monitoreo**: Instala plugins como Jetpack o utiliza servicios externos como Google Analytics o Sucuri para monitorear tráfico y actividad. | - **Herramientas de Monitoreo**: Instala plugins como Jetpack o utiliza servicios externos como Google Analytics o Sucuri para monitorear tráfico y actividad. |
| **10. Desactiva Editor de Archivos** | - **Modificar wp-config.php**: Abre el archivo wp-config.php ubicado en `/var/www/html/tu_dominio/wp-config.php` y agrega: `<br> define('DISALLOW_FILE_EDIT', true);` | - **Modificar wp-config.php**: Abre el archivo wp-config.php ubicado en `/var/www/html/tu_dominio/wp-config.php` y agrega: `<br> define('DISALLOW_FILE_EDIT', true);` |

---

## Notas Adicionales

### Estructura de Directorios de WordPress:

- `/var/www/html/tu_dominio/`: Directorio raíz de tu instalación de WordPress.
  - `/wp-admin/`: Archivos del panel de administración.
  - `/wp-content/`: Temas y plugins.
  - `/wp-includes/`: Archivos principales de WordPress.
  - `wp-config.php`: Archivo de configuración principal.

### Reiniciar Servicios:

- **Nginx**: `sudo systemctl restart nginx`
- **Apache**: `sudo systemctl restart apache2`

### Comprobación de Seguridad:

Revisa periódicamente los registros de acceso y errores en:
- `/var/log/nginx/` (para Nginx)
- `/var/log/apache2/` (para Apache)  
para detectar actividades sospechosas.

-
