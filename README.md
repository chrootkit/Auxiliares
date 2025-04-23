# Auxiliares
# Crear un archivo .txt con los comandos organizados por módulo

comandos_txt = """
MÓDULO I: Tareas básicas de administración
------------------------------------------

Archivos y directorios
-----------------------
ls              # Lista archivos
cd              # Cambia de directorio
pwd             # Muestra ruta actual
cp archivo destino   # Copiar archivos
mv archivo destino   # Mover/renombrar archivos
rm archivo      # Eliminar archivo
mkdir carpeta   # Crear directorio
rmdir carpeta   # Eliminar directorio vacío
touch archivo   # Crear archivo vacío
cat, less, more archivo   # Ver contenido

Gestión de usuarios y permisos
------------------------------
adduser nombre_usuario          # Crear usuario
passwd nombre_usuario           # Asignar contraseña
usermod -aG grupo usuario       # Agregar usuario a grupo
deluser nombre_usuario          # Eliminar usuario
chmod 755 archivo               # Cambiar permisos
chown usuario:grupo archivo     # Cambiar dueño

Configuración de red
---------------------
ip a                            # Ver IP
nmcli con show                  # Mostrar conexiones
nmcli con up 'nombre'          # Activar interfaz
nmtui                           # Interfaz de configuración en consola
ping google.com                 # Verificar conexión


MÓDULO II: Sistemas operativos en ejecución
-------------------------------------------

Gestión de paquetes (dnf/yum)
-----------------------------
dnf update                      # Actualizar sistema
dnf install paquete             # Instalar paquete
dnf remove paquete              # Eliminar paquete
dnf search paquete              # Buscar paquete
dnf info paquete                # Información de paquete

Procesos y servicios
---------------------
top                            # Monitor de procesos
ps aux                         # Lista procesos
kill PID                       # Terminar proceso
systemctl status servicio      # Estado de servicio
systemctl start/stop/restart servicio  # Gestionar servicios
systemctl enable servicio      # Activar en arranque

Tareas programadas
-------------------
crontab -e                     # Editar tareas del usuario
systemctl list-timers          # Ver temporizadores (timers)


MÓDULO III: Avanzado
---------------------

Kernel y arranque
------------------
uname -r                       # Versión del kernel
journalctl -b                  # Logs del arranque

Bash y scripting
-----------------
#!/bin/bash                    # Encabezado script
echo "Hola Mundo"             # Mostrar texto
for i in {1..5}; do echo $i; done  # Bucle


MÓDULO IV: Servicios de red
----------------------------

SSH
---
systemctl start sshd
systemctl enable sshd

Apache y NGINX
---------------
dnf install httpd              # Instalar Apache
systemctl start httpd
firewall-cmd --permanent --add-service=http
firewall-cmd --reload

dnf install nginx              # Instalar NGINX
systemctl start nginx

FTP, NFS, Correo
----------------
dnf install vsftpd
systemctl start vsftpd

dnf install nfs-utils
systemctl start nfs-server


MÓDULO VI: Seguridad
---------------------
getenforce                     # Ver estado de SELinux
setenforce 0                   # Desactivar temporalmente SELinux
firewall-cmd --list-all        # Ver configuración del firewall
firewall-cmd --add-port=8080/tcp --permanent


MÓDULO VII: LDAP, Samba
------------------------
dnf install openldap-servers openldap-clients
dnf install samba samba-common samba-client
"""



