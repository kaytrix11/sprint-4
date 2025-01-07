Evolución del Proyecto
17/12/2024
Autenticación SSH basada en clave pública: Se configuró la autenticación basada en clave pública, eliminando el uso de contraseñas. Se generaron y distribuyeron las claves SSH para el acceso remoto.

Cambio de puerto por defecto: Se cambió el puerto de escucha SSH de 22 a 2222 para mejorar la seguridad y evitar ataques automatizados dirigidos al puerto por defecto.

Vinculación IP (opcional): Se configuró el servicio SSH para que solo escuche en una dirección IP específica del servidor, limitando el acceso a esa IP para mayor seguridad.

Deshabilitar el usuario ROOT para login: Se deshabilitó el acceso al usuario root para evitar que los atacantes intenten acceder con privilegios de administrador.

Limitar el acceso SSH a usuarios específicos: Se configuró el acceso SSH para que solo usuarios específicos puedan acceder al servidor mediante SSH, restringiendo otros accesos.

Deshabilitar inicio de sesión basado en contraseña: Se deshabilitó la autenticación basada en contraseñas, obligando a los usuarios a utilizar claves SSH para autenticar su acceso.

Deshabilitar contraseñas vacías: Se deshabilitó el uso de contraseñas vacías para las cuentas de usuario, aumentando la seguridad general del sistema.

Limitar intentos de autenticación fallidos: Se limitó el número de intentos fallidos de autenticación, evitando que un atacante pueda probar múltiples combinaciones de contraseñas en un corto periodo de tiempo.

Limitar conexiones simultáneas no autenticadas: Se configuró el sistema para limitar el número de conexiones no autenticadas simultáneas, previniendo abusos en el acceso al servidor.

Habilitar un banner de advertencia: Se habilitó un banner de advertencia que se muestra a los usuarios antes de que inicien sesión, informándoles de las políticas de acceso.

Configurar tiempo de espera de inactividad: Se configuró un tiempo de espera para cerrar automáticamente las sesiones inactivas, liberando recursos y mejorando la seguridad.

Deshabilitar X11Forwarding: Se deshabilitó el reenvío de X11 para evitar que las aplicaciones gráficas se ejecuten de forma remota y aumentar la seguridad.

Configurar Chroot para usuarios: Se configuró el uso de chroot para restringir a ciertos usuarios a su directorio de inicio, mejorando el aislamiento y la seguridad.

06/01/2025
Instalación y configuración de Google Authenticator: Se instaló el paquete libpam-google-authenticator y se configuró el doble factor de autenticación (2FA) en SSH. Esto requiere que los usuarios no solo ingresen su contraseña (o clave SSH), sino que también proporcionen un código de autenticación generado por una aplicación como Google Authenticator.

Configuración del archivo PAM para Google Authenticator: Se editó el archivo /etc/pam.d/sshd para integrar Google Authenticator en el proceso de autenticación SSH, asegurando que se aplique 2FA.

Configuración de SSH para aceptar 2FA: Se modificó el archivo /etc/ssh/sshd_config para habilitar el uso de autenticación de desafío-respuesta y aceptar la autenticación mediante Google Authenticator.
