# Proyecto Ansible + Vagrant para Desplegar WordPress

Este proyecto usa **Vagrant** y **Ansible** para desplegar automáticamente un sitio **WordPress** en una máquina virtual. Además, configura **NGINX** para redirigir el tráfico del puerto 80 al 8080 y restringe el acceso a las páginas de administración y login de WordPress.

## Pre-requisitos
Antes de ejecutar este proyecto, asegúrate de tener instalados los siguientes programas en tu máquina:

- [VirtualBox](https://www.virtualbox.org/)
- [Vagrant](https://www.vagrantup.com/)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Instalación y Ejecución
Sigue estos pasos para desplegar WordPress:

1. Clona este repositorio o extrae el código en un directorio de tu máquina.
2. Abre una terminal y navega hasta el directorio del proyecto.
3. Ejecuta el siguiente comando para iniciar la máquina virtual y aprovisionarla:
   ```sh
   vagrant up
   ```
   Este proceso puede tardar algunos minutos, ya que instalará todos los componentes necesarios.

## Configuración de NGINX
El archivo de configuración de **NGINX** realiza las siguientes tareas:
- Redirige las peticiones del puerto **80** al **8080**.
- Restringe el acceso a `/wp-admin` y `/wp-login.php` permitiendo solo ciertos IPs (ajustable en `provisioning/templates/wordpress.conf.j2`).

## Pruebas
Una vez finalizada la instalación:

1. Abre tu navegador y accede a `http://{VM_IP}` para ver el sitio WordPress funcionando.
2. Para verificar la restricción de acceso, intenta acceder a `http://{VM_IP}/wp-admin` o `http://{VM_IP}/wp-login.php` desde una IP no permitida.

## Destruir la Máquina Virtual
Para eliminar completamente la máquina virtual y liberar espacio:
```sh
vagrant destroy -f
```

## Licencia
Este proyecto está bajo la licencia **MIT**.
